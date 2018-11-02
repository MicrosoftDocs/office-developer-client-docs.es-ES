---
title: Recordset2.AddNew (método) (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67ddd40c6973b323820efbfa67d14c88f0c0b21a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928813"
---
# <a name="recordset2addnew-method-dao"></a>Recordset2.AddNew (método) (DAO)


**Se aplica a**: Access 2013, Office 2013
 

Crea un nuevo registro para un objeto **Recordset2** actualizable.

## <a name="syntax"></a>Sintaxis

*expresión* . AddNew

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

Utilice el método **AddNew** para crear y agregar un nuevo registro al objeto **Recordset2** designado por el conjunto de registros. Este método establece los campos en sus valores predeterminados y, si no especifica ningún valor, establece los campos en Null (valores predeterminados especificados para un objeto **Recordset2** de tipo tabla).

Tras modificar el nuevo registro, use el método **[Update](recordset2-update-method-dao.md)** para guardar los cambios y agregar el registro a **Recordset2**. No se producen cambios en la base de datos hasta que use el método **Update**.


> [!NOTE]
> <P>[!NOTA] Si usa <STRONG>AddNew</STRONG> y ejecuta luego cualquier operación para desplazarse a otro registro pero sin usar <STRONG>Update</STRONG>, los cambios se pierden sin advertencia. Además, si cierra <STRONG>Recordset2</STRONG> o termina el procedimiento que declara el objeto <STRONG>Recordset2</STRONG> o su objeto <STRONG><A href="database-object-dao.md">Database</A></STRONG>, el nuevo registro se descarta sin advertencia.</P>




> [!NOTE]
> <P>[!NOTA] Cuando utiliza <STRONG>AddNew</STRONG> en un área de trabajo de Microsoft Access y el motor de base de datos debe crear una nueva página para contener el registro actual, el bloqueo de página es pesimista. Si el nuevo registro cabe en una página existente, el bloqueo de página es optimista.</P>



Si no se desplazó al último registro del objeto **Recordset2**, se pueden incluir los registros agregados a las tablas base por otros procesos si están colocados más allá del registro activo. Si agrega un registro a su propio objeto **Recordset2**, no obstante, el registro estará visible en **Recordset2** y se incluirá en la tabla subyacente donde estará visible para cualquier nuevo objeto **Recordset2**.

La posición del nuevo registro depende del tipo de **Recordset2**:

  - En un objeto **Recordset2** de tipo dynaset, los registros se insertan al final de **Recordset**, independientemente de las reglas de clasificación u ordenación que hubiera en vigor cuando se abrió **Recordset**.

  - En un objeto **Recordset2** de tipo tabla cuya propiedad **[Index](recordset2-index-property-dao.md)** se definió, los registros se devuelven al lugar correspondiente según el criterio de ordenación. Si no definió la propiedad **Index**, los nuevos registros se devuelven al final de **Recordset**.

El registro que estaba activo antes de utilizar **AddNew** sigue estando activo. Si desea que el nuevo registro sea el activo, puede establecer la propiedad **[Bookmark](recordset2-bookmark-property-dao.md)** en el marcador identificado por el valor de la propiedad **[LastModified](recordset2-lastmodified-property-dao.md)**.


> [!NOTE]
> <P>[!NOTA] Para agregar, editar o eliminar un registro, debe haber un índice único en el registro del origen de datos subyacente. En caso contrario, se produce un error de "denegación de permiso" en la llamada al método <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG> o <STRONG>Edit</STRONG> en un área de trabajo de Microsoft Access.</P>



## <a name="example"></a>Ejemplo

En este ejemplo se utiliza el método **AddNew** para crear un registro nuevo con el nombre especificado. Se requiere la función AddName para que pueda ejecutarse este procedimiento.

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
