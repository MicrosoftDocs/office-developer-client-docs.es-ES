---
title: Properties Collection (DAO)
TOCTitle: Properties Collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f30ccd48ee5e4f4815be4d7e1ec6d94f237bc16
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874289"
---
# <a name="properties-collection-dao"></a>Properties Collection (DAO)


**Se aplica a**: Access 2013, Office 2013

Una colección **Properties** contiene todos los objetos **[Property](property-object-dao.md)** de una instancia específica de un objeto.

## <a name="remarks"></a>Observaciones

Todos los objetos DAO, salvo los objetos **Connection** y **Error**, contienen una colección **Properties**, que tiene varios objetos **Property** integrados. Estos objetos **Property** (que a menudo se denominan propiedades) caracterizan de manera única esa instancia del objeto.

Además de las propiedades integradas, también puede crear y agregar sus propias propiedades definidas por el usuario. Para agregar una propiedad definida por el usuario a una instancia existente de un objeto, primero debe definir sus características con el método **CreateProperty** y después agregarla a la colección con el método **Append**. Si se hace referencia a un objeto **Property** definido por el usuario que aún no ha sido anexado a una colección **Properties**, se producirá un error, y lo mismo ocurre al anexar un objeto **Property** definido por el usuario a una colección **Properties** que contiene un objeto **Property** del mismo nombre.

Puede utilizar el método **Delete** para quitar propiedades definidas por el usuario de la colección **Properties**, pero no puede quitar propiedades integradas.


> [!NOTE]
> <P>[!NOTA] Un objeto <STRONG>Property</STRONG> definido por el usuario sólo está asociado con la instancia concreta de un objeto. La propiedad no está definida para todas las instancias de objetos del tipo seleccionado.</P>



Para hacer referencia a un objeto **Property** integrado en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:

objeto. **Propiedades** (0)

objeto. **Propiedades** ("nombre")

objeto. **Propiedades** \! \[nombre\]

Para una propiedad integrada, también se puede usar la siguiente sintaxis:

objeto.Name


> [!NOTE]
> <P>Para una propiedad definida por el usuario, debe usar el objeto completo. <STRONG>Propiedades</STRONG> sintaxis ("nombre").</P>



Con las misma formas sintácticas, se puede hacer referencia también a la propiedad **Value** de un objeto **Property**. El contexto de la referencia determinará si hace referencia al propio objeto **Property** o a la propiedad **Value** del objeto **Property**.

## <a name="example"></a>Ejemplo

En este ejemplo se crea una propiedad definida por el usuario para la base de datos actual, se establecen sus propiedades **Type** y **Value** y se agrega a la colección **Properties** de la base de datos. A continuación, se enumeran todas las propiedades de la base de datos.

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

En este ejemplo se intenta establecer el valor de una propiedad definida por el usuario. Si la propiedad no existe, se utiliza el método **CreateProperty** para crear y definir el valor de la nueva propiedad. Se requiere el procedimiento SetProperty para que pueda ejecutarse este procedimiento.

```vb
    Sub CreatePropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Set the Archive property to True. 
     SetProperty dbsNorthwind, "Archive", True 
     
     With dbsNorthwind 
     Debug.Print "Properties of " & .Name 
     
     ' Enumerate Properties collection of the Northwind 
     ' database. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     
     ' Delete the new property since this is a 
     ' demonstration. 
     .Properties.Delete "Archive" 
     
     .Close 
     End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
     booTemp As Boolean) 
     
     Dim prpNew As Property 
     Dim errLoop As Error 
     
     ' Attempt to set the specified property. 
     On Error GoTo Err_Property 
     dbsTemp.Properties("strName") = booTemp 
     On Error GoTo 0 
     
     Exit Sub 
     
    Err_Property: 
     
     ' Error 3270 means that the property was not found. 
     If DBEngine.Errors(0).Number = 3270 Then 
     ' Create property, set its value, and append it to the 
     ' Properties collection. 
     Set prpNew = dbsTemp.CreateProperty(strName, _ 
     dbBoolean, booTemp) 
     dbsTemp.Properties.Append prpNew 
     Resume Next 
     Else 
     ' If different error has occurred, display message. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End 
     End If 
     
    End Sub
```
