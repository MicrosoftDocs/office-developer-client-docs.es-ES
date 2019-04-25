---
title: Objeto DBEngine (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 479eff80d25279a1c5e918a3b639443ad3b25c6c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294277"
---
# <a name="dbengine-object-dao"></a>Objeto DBEngine (DAO)

**Se aplica a:** Access 2013, Office 2013

El objeto **DBEngine** es el objeto de nivel superior en el modelo de objetos DAO.

## <a name="remarks"></a>Comentarios

El objeto **DBEngine** contiene y controla todos los demás objetos de la jerarquía de objetos DAO. No puede crear objetos **DBEngine** adicionales y el objeto **DBEngine** no es un elemento de ninguna colección.

Con cualquier tipo de base de datos o conexión puede:

  - Utilizar la propiedad **Version** para obtener el número de versión DAO.

  - Usar la propiedad **LoginTimeout** para obtener o establecer el tiempo de espera de inicio de sesión de ODBC y el método **RegisterDatabase** para proporcionar información de ODBC al motor de base de datos de Microsoft Access.

  - Usar las propiedades **DefaultPassword** y **DefaultUser** a fin de establecer la identificación de usuario y la contraseña para el objeto **Workspace** predeterminado.

  - Utilizar el método **CreateWorkspace** para crear un nuevo objeto **Workspace**. Puede emplear argumentos opcionales para anular la configuración de las propiedades **DefaultType**, **DefaultPassword** y **DefaultUser**.

  - Usar el método **OpenDatabase** para abrir una base de datos en el objeto **Workspace** predeterminado y utilizar los métodos **BeginTrans**, **Commit** y **Rollback** para controlar las transacciones en el objeto **Workspace** predeterminado.

  - Utilizar la colección **Workspaces** para hacer referencia a objetos **Workspace** específicos.

  - Usar la colección **Errors** para examinar los detalles de errores de acceso a datos.

Otras propiedades y métodos sólo están disponibles cuando utiliza DAO con el motor de base de datos de Microsoft Access. Puede utilizarlos para controlar el motor de base de datos de Microsoft Access, modificar sus propiedades y realizar tareas en objetos temporales que no son elementos de colecciones. Por ejemplo, puede:

  - Utilizar el método **CreateDatabase** para crear un nuevo objeto **Database** del motor de base de datos de Microsoft Access.

  - Usar el método **Idle** para que el motor de base de datos de Microsoft Access pueda completar todas las tareas pendientes.

  - Utilizar los métodos **CompactDatabase** y **RepairDatabase** para mantener los archivos de bases de datos.

  - Usar las propiedades **IniPath** y **SystemDB** para especificar la ubicación de la información del Registro de Windows para el motor de base de datos de Microsoft Access y el archivo de información de grupo de trabajo de Microsoft Access respectivamente. El método **SetOption** le permite anular la configuración del Registro de Windows para el motor de base de datos de Microsoft Access.

Una vez modificados los valores de las propiedades **DefaultType** y **IniPath**, sólo los objetos **Workspace** posteriores reflejarán estos cambios.

Para hacer referencia a una colección que pertenece al objeto **DBEngine**, o a un método o propiedad que se aplica a este objeto, utilice la sintaxis siguiente:

\[**DBEngine**.\]\[colección | método | propiedad\]

## <a name="example"></a>Ejemplo

En este ejemplo se enumeran las colecciones del objeto **DBEngine**.

```vb
    Sub DBEngineX() 
     
     Dim wrkLoop As Workspace 
     Dim prpLoop As Property 
     
     With DBEngine 
     Debug.Print "DBEngine Properties" 
     
     ' Enumerate Properties collection of DBEngine, 
     ' trapping for properties whose values are 
     ' invalid in this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " _ 
     & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Debug.Print "Workspaces collection of DBEngine" 
     
     ' Enumerate Workspaces collection of DBEngine. 
     For Each wrkLoop In .Workspaces 
     Debug.Print " " & wrkLoop.Name 
     
     ' Enumerate Properties collection of each 
     ' Workspace object, trapping for properties 
     ' whose values are invalid in this context. 
     For Each prpLoop In wrkLoop.Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Next wrkLoop 
     
     End With 
     
    End Sub
```
