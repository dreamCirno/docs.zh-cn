---
description: 了解详细信息：更新数据源中的数据
title: 更新数据源中的数据
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 55c545e5-dcd5-4323-a5b9-3825c2157462
ms.openlocfilehash: a55d6a53f4607908fa279474419803eac3963909
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99766564"
---
# <a name="updating-data-in-a-data-source"></a>更新数据源中的数据

修改数据的 SQL 语句（如 INSERT、UPDATE 或 DELETE）不返回行。 同样，许多存储过程执行操作但不返回行。 要执行不返回行的命令，使用相应 SQL 命令创建一个 Command 对象，并创建一个 Connection，包括所有必需的 Parameters。 通过 **命令** 对象的 **ExecuteNonQuery** 方法执行该命令。  
  
 ExecuteNonQuery 方法返回一个整数，表示受已执行的语句或存储过程影响的行数。 如果执行了多个语句，则返回的值为受所有已执行语句影响的记录的总数。  
  
## <a name="example"></a>示例  

 以下代码示例执行一个 INSERT 语句，以使用 ExecuteNonQuery 将一个记录插入数据库中。  
  
```vb  
' Assumes connection is a valid SqlConnection.  
connection.Open()  
  
Dim queryString As String = "INSERT INTO Customers " & _  
  "(CustomerID, CompanyName) Values('NWIND', 'Northwind Traders')"  
  
Dim command As SqlCommand = New SqlCommand(queryString, connection)  
Dim recordsAffected As Int32 = command.ExecuteNonQuery()  
```  
  
```csharp  
// Assumes connection is a valid SqlConnection.  
connection.Open();  
  
string queryString = "INSERT INTO Customers " +  
  "(CustomerID, CompanyName) Values('NWIND', 'Northwind Traders')";  
  
SqlCommand command = new SqlCommand(queryString, connection);  
Int32 recordsAffected = command.ExecuteNonQuery();  
```  
  
 以下代码示例执行由[执行编录操作](performing-catalog-operations.md)中的示例代码创建的存储过程。 该存储过程没有返回任何行，因此将使用 ExecuteNonQuery 方法，但该存储过程会接收输入参数并返回输出参数和返回值。  
  
 对于 <xref:System.Data.OleDb.OleDbCommand> 对象，必须先将 **ReturnValue** 参数添加到 **Parameters** 集合。  
  
```vb  
' Assumes connection is a valid SqlConnection.  
Dim command As SqlCommand = _  
   New SqlCommand("InsertCategory" , connection)  
command.CommandType = CommandType.StoredProcedure  
  
Dim parameter As SqlParameter = _  
 command.Parameters.Add("@RowCount", SqlDbType.Int)  
parameter.Direction = ParameterDirection.ReturnValue  
  
parameter = command.Parameters.Add( _  
  "@CategoryName", SqlDbType.NChar, 15)  
  
parameter = command.Parameters.Add("@Identity", SqlDbType.Int)  
parameter.Direction = ParameterDirection.Output  
  
command.Parameters("@CategoryName").Value = "New Category"  
command.ExecuteNonQuery()  
  
Dim categoryID As Int32 = CInt(command.Parameters("@Identity").Value)  
Dim rowCount As Int32 = CInt(command.Parameters("@RowCount").Value)
```  
  
```csharp  
// Assumes connection is a valid SqlConnection.  
SqlCommand command = new SqlCommand("InsertCategory" , connection);  
command.CommandType = CommandType.StoredProcedure;  
  
SqlParameter parameter = command.Parameters.Add(  
  "@RowCount", SqlDbType.Int);  
parameter.Direction = ParameterDirection.ReturnValue;  
  
parameter = command.Parameters.Add(  
  "@CategoryName", SqlDbType.NChar, 15);  
  
parameter = command.Parameters.Add("@Identity", SqlDbType.Int);  
parameter.Direction = ParameterDirection.Output;  
  
command.Parameters["@CategoryName"].Value = "New Category";  
command.ExecuteNonQuery();  
  
Int32 categoryID = (Int32) command.Parameters["@Identity"].Value;  
Int32 rowCount = (Int32) command.Parameters["@RowCount"].Value;  
```  
  
## <a name="see-also"></a>请参阅

- [使用命令修改数据](using-commands-to-modify-data.md)
- [使用 DataAdapter 更新数据源](updating-data-sources-with-dataadapters.md)
- [命令和参数](commands-and-parameters.md)
- [ADO.NET 概述](ado-net-overview.md)
