---
title: ActiveX de objetos de datos de datos (ADO)
TOCTitle: ADO errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5a25dc0d1d5e621a610b34ca1875c3fd76ba56eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283383"
---
# <a name="ado-errors"></a>Errores de ADO

**Se aplica a:** Access 2013, Office 2013

Los errores de ADO se notifican a su programa como errores en tiempo de ejecución. Puede usar el mecanismo de interceptación de errores de su lenguaje de programación para interceptarlos y controlarlos. Por ejemplo, en Visual Basic, use la instrucción **On Error**. En Visual J++, use un bloque **try-catch**. En Visual C++, depende del método que esté usando para obtener acceso a las bibliotecas ADO. Con \# la importación, use un **bloque try-catch.** De lo contrario, los programadores de C++ tienen que recuperar explícitamente el objeto de error llamando a **GetErrorInfo**. El siguiente procedimiento Sub de Visual Basic muestra cómo interceptar un error en ADO:

```vb 
 
' BeginErrorHandlingVB01 
Private Sub Form_Load() 
 ' Turn on error handling 
 On Error GoTo FormLoadError 
 
 'Open the database and the recordset for processing. 
 ' 
 Dim strCnn As String 
 strCnn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 
 ' cnn is a Public Connection Object because 
 ' it was defined WithEvents 
 Set cnn = New ADODB.Connection 
 cnn.Open strCnn 
 
 ' The next line of code intentionally causes 
 ' an error by trying to open a connection 
 ' that has already been opened. 
 cnn.Open strCnn 
 
 ' rst is a Public Recordset because it 
 ' was defined WithEvents 
 Set rst = New ADODB.Recordset 
 rst.Open "Customers", cnn 
 
 Exit Sub 
 
' Error handler 
FormLoadError: 
 Dim strErr As String 
 Select Case Err 
 Case adErrObjectOpen 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 strErr = strErr & "Error reported by: " & Err.Source & vbCrLf 
 strErr = strErr & "Help File: " & Err.HelpFile & vbCrLf 
 strErr = strErr & "Topic ID: " & Err.HelpContext 
 MsgBox strErr 
 Debug.Print strErr 
 Err.Clear 
 Resume Next 
 ' If some other error occurs that 
 ' has nothing to do with ADO, show 
 ' the number and description and exit. 
 Case Else 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 MsgBox strErr 
 Debug.Print strErr 
 Unload Me 
 End Select 
End Sub 
' EndErrorHandlingVB01 
```

Este **procedimiento de evento \_ De** carga de formulario crea intencionalmente un error al intentar abrir el mismo objeto **Connection** dos veces. La segunda vez que se llama al método **Open**, se activa el controlador de errores. En este caso, el error es de tipo **adErrObjectOpen**, de modo que el controlador de errores muestra el siguiente mensaje antes de reanudar la ejecución del programa:

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

El mensaje de error incluye cada información proporcionada por el objeto **Err** de Visual Basic, excepto el valor **LastDLLError**, que no se aplica aquí. El número de error indica qué error se ha producido. La descripción es útil en los casos en los que no desea controlar el error usted mismo. Simplemente, se lo puede pasar al usuario. Aunque normalmente deseará utilizar mensajes personalizados para su aplicación, no puede prever cada error; la descripción proporciona algunas pistas con respecto a qué falló. En el código de ejemplo, la información sobre el error procedía del objeto **Connection**. Aquí verá el tipo o el identificador mediante programación del objeto, y no un nombre de variable.


> [!NOTE]
> [!NOTA] El objeto **Err** de Visual Basic sólo contiene información acerca del error más reciente. La colección **Errors** de ADO del objeto **Connection** contiene un objeto **Error** por cada error generado por la operación de ADO más reciente. Utilice la colección **Errors** en vez de el objeto **Err** para controlar varios errores. Para obtener más información acerca de la colección **Errors**, vea <A href="provider-errors.md">Errores del proveedor</A>. Sin embargo, si no hay ningún objeto **Connection** válido, el objeto **Err** es la única fuente de información sobre errores de ADO.

¿Qué tipos de operaciones tienen más probabilidad de provocar errores de ADO? Los errores más comunes de ADO pueden conllevar que se abra un objeto como **Connection** o **Recordset**, que se intente actualizar datos, o que se llame a un método o a una propiedad no admitidos por su proveedor.

También se pueden pasar errores de OLE DB a su aplicación como errores en tiempo de ejecución de la colección **Errors**. Para obtener más información acerca de números de error en OLE DB, vea el capítulo 16 de la Referencia del programador de OLE DB.

