---
title: Errores de ActiveX Data Objects (ADO)
TOCTitle: ADO errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5a25dc0d1d5e621a610b34ca1875c3fd76ba56eb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720859"
---
# <a name="ado-errors"></a><span data-ttu-id="1fec4-102">Errores de ADO</span><span class="sxs-lookup"><span data-stu-id="1fec4-102">ADO errors</span></span>

<span data-ttu-id="1fec4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1fec4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1fec4-104">Los errores de ADO se notifican a su programa como errores en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1fec4-104">ADO Errors are reported to your program as run-time errors.</span></span> <span data-ttu-id="1fec4-105">Puede usar el mecanismo de interceptación de errores de su lenguaje de programación para interceptarlos y controlarlos.</span><span class="sxs-lookup"><span data-stu-id="1fec4-105">You can use the error-trapping mechanism of your programming language to trap and handle them.</span></span> <span data-ttu-id="1fec4-106">Por ejemplo, en Visual Basic, use la instrucción **On Error**.</span><span class="sxs-lookup"><span data-stu-id="1fec4-106">For example, in Visual Basic, use the **On Error** statement.</span></span> <span data-ttu-id="1fec4-107">En Visual J++, use un bloque **try-catch**.</span><span class="sxs-lookup"><span data-stu-id="1fec4-107">In Visual J++, use a **try-catch** block.</span></span> <span data-ttu-id="1fec4-108">En Visual C++, depende del método que esté usando para obtener acceso a las bibliotecas ADO.</span><span class="sxs-lookup"><span data-stu-id="1fec4-108">In Visual C++, it depends on the method you are using to access the ADO libraries.</span></span> <span data-ttu-id="1fec4-109">Con \#importar, utilice un bloque **try-catch** .</span><span class="sxs-lookup"><span data-stu-id="1fec4-109">With \#import, use a **try-catch** block.</span></span> <span data-ttu-id="1fec4-110">De lo contrario, los programadores de C++ tienen que recuperar explícitamente el objeto de error llamando a **GetErrorInfo**.</span><span class="sxs-lookup"><span data-stu-id="1fec4-110">Otherwise, C++ programmers need to explicitly retrieve the error object by calling **GetErrorInfo**.</span></span> <span data-ttu-id="1fec4-111">El siguiente procedimiento Sub de Visual Basic muestra cómo interceptar un error en ADO:</span><span class="sxs-lookup"><span data-stu-id="1fec4-111">The following Visual Basic sub procedure demonstrates trapping an ADO error:</span></span>

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

<span data-ttu-id="1fec4-112">Esto **formulario\_carga** procedimiento de evento intencionadamente crea un error al intentar abrir dos veces el mismo objeto de **conexión** .</span><span class="sxs-lookup"><span data-stu-id="1fec4-112">This **Form\_Load** event procedure intentionally creates an error by trying to open the same **Connection** object twice.</span></span> <span data-ttu-id="1fec4-113">La segunda vez que se llama al método **Open**, se activa el controlador de errores.</span><span class="sxs-lookup"><span data-stu-id="1fec4-113">The second time the **Open** method is called, the error handler is activated.</span></span> <span data-ttu-id="1fec4-114">En este caso, el error es de tipo **adErrObjectOpen**, de modo que el controlador de errores muestra el siguiente mensaje antes de reanudar la ejecución del programa:</span><span class="sxs-lookup"><span data-stu-id="1fec4-114">In this case the error is of type **adErrObjectOpen**, so the error handler displays the following message before resuming program execution:</span></span>

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

<span data-ttu-id="1fec4-p103">El mensaje de error incluye cada información proporcionada por el objeto **Err** de Visual Basic, excepto el valor **LastDLLError**, que no se aplica aquí. El número de error indica qué error se ha producido. La descripción es útil en los casos en los que no desea controlar el error usted mismo. Simplemente, se lo puede pasar al usuario. Aunque normalmente deseará utilizar mensajes personalizados para su aplicación, no puede prever cada error; la descripción proporciona algunas pistas con respecto a qué falló. En el código de ejemplo, la información sobre el error procedía del objeto **Connection**. Aquí verá el tipo o el identificador mediante programación del objeto, y no un nombre de variable.</span><span class="sxs-lookup"><span data-stu-id="1fec4-p103">The error message includes each piece of information provided by the Visual Basic **Err** object except for the **LastDLLError** value, which does not apply here. The error number tells you which error has occurred. The description is useful in cases in which you do not want to handle the error yourself. You can simply pass it along to the user. Although you will usually want to use messages customized for your application, you cannot anticipate every error; the description gives some clue as to what went wrong. In the sample code, the error was reported by the **Connection** object. You will see the object's type or programmatic ID here — not a variable name.</span></span>


> [!NOTE]
> <span data-ttu-id="1fec4-p104">[!NOTA] El objeto **Err** de Visual Basic sólo contiene información acerca del error más reciente. La colección **Errors** de ADO del objeto **Connection** contiene un objeto **Error** por cada error generado por la operación de ADO más reciente. Utilice la colección **Errors** en vez de el objeto **Err** para controlar varios errores. Para obtener más información acerca de la colección **Errors**, vea <A href="provider-errors.md">Errores del proveedor</A>. Sin embargo, si no hay ningún objeto **Connection** válido, el objeto **Err** es la única fuente de información sobre errores de ADO.</span><span class="sxs-lookup"><span data-stu-id="1fec4-p104">The Visual Basic **Err** object only contains information about the most recent error. The ADO **Errors** collection of the **Connection** object contains one **Error** object for each error raised by the most recent ADO operation. Use the **Errors** collection rather than the **Err** object to handle multiple errors. For more information about the **Errors** collection, see <A href="provider-errors.md">Provider Errors</A>. However, if there is no valid **Connection** object, the **Err** object is the only source for information about ADO errors.</span></span>

<span data-ttu-id="1fec4-p105">¿Qué tipos de operaciones tienen más probabilidad de provocar errores de ADO? Los errores más comunes de ADO pueden conllevar que se abra un objeto como **Connection** o **Recordset**, que se intente actualizar datos, o que se llame a un método o a una propiedad no admitidos por su proveedor.</span><span class="sxs-lookup"><span data-stu-id="1fec4-p105">What kinds of operations are likely to cause ADO errors? Common ADO errors can involve opening an object such as a **Connection** or **Recordset**, attempting to update data, or calling a method or property that is not supported by your provider.</span></span>

<span data-ttu-id="1fec4-p106">También se pueden pasar errores de OLE DB a su aplicación como errores en tiempo de ejecución de la colección **Errors**. Para obtener más información acerca de números de error en OLE DB, vea el capítulo 16 de la Referencia del programador de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1fec4-p106">OLE DB errors can also be passed to your application as run-time errors in the **Errors** collection. For more information about OLE DB error numbers, see Chapter 16 of the OLE DB Programmer's Reference.</span></span>

