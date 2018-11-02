---
title: 'Objetos de objeto de error: acceso a datos (DAO)'
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e373dd683e679737564d44057ec0b96a866ab84e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923479"
---
# <a name="error-object-dao"></a><span data-ttu-id="58046-102">Objeto Error (DAO)</span><span class="sxs-lookup"><span data-stu-id="58046-102">Error object (DAO)</span></span>


<span data-ttu-id="58046-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="58046-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="58046-104">El objeto **Error** contiene detalles sobre los errores de acceso a datos, cada uno de los cuales pertenece a una operación única que implica a DAO.</span><span class="sxs-lookup"><span data-stu-id="58046-104">**Error** object contains details about data access errors, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="58046-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58046-105">Remarks</span></span>

<span data-ttu-id="58046-p101">Cualquier operación que implica a DAO puede generar uno o varios errores. Por ejemplo, una llamada a un servidor ODBC puede provocar un error del servidor de base de datos, un error de ODBC o de DAO. Cuando se produce uno de estos errores, se coloca un objeto **Error** en la colección **Errors** del objeto **DBEngine**. Un único evento puede provocar, por lo tanto, varios objetos **Error** que aparecen en la colección **Errors**.</span><span class="sxs-lookup"><span data-stu-id="58046-p101">Any operation involving DAO can generate one or more errors. For example, a call to an ODBC server might result in an error from the database server, an error from ODBC, and a DAO error. As each such error occurs, an **Error** object is placed in the **Errors** collection of the **DBEngine** object. A single event can therefore result in several **Error** objects appearing in the **Errors** collection.</span></span>

<span data-ttu-id="58046-p102">Cuando una operación DAO posterior genera un error, se borra la colección **Errors** y uno o varios objetos nuevos **Error** se colocan en la colección **Errors**. Las operaciones DAO que no generan errores no tienen efecto en la colección **Errors**.</span><span class="sxs-lookup"><span data-stu-id="58046-p102">When a subsequent DAO operation generates an error, the **Errors** collection is cleared, and one or more new **Error** objects are placed in the **Errors** collection. DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="58046-p103">El conjunto de objetos **Error** en la colección **Errors** describe un único error. El primer objeto **Error** es el error de nivel más bajo (el error de origen), el segundo, el error de nivel inmediatamente superior, etc. Por ejemplo, si se produce un error de ODBC mientras intenta abrir un objeto **[Recordset](recordset-object-dao.md)**, el primer objeto **Error**  **Errors**(0) contiene el nivel de error de ODBC más bajo; los errores posteriores contienen los errores de ODBC devueltos por las distintas capas de ODBC. En este caso, el administrador de controladores ODBC, y posiblemente el controlador mismo, devuelven objetos **Error** separados. El último objeto **Error**  **Errors.Count-** 1 contiene el error de DAO que indica que no se pudo abrir el objeto.</span><span class="sxs-lookup"><span data-stu-id="58046-p103">The set of **Error** objects in the **Errors** collection describes one error. The first **Error** object is the lowest level error (the originating error), the second the next higher level error, and so forth. For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first **Error** object— **Errors**(0)— contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC. In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects. The last **Error** object— **Errors.Count-** 1— contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="58046-p104">Enumerar los errores específicos en la colección **Errors** permite rutinas de tratamiento de errores para determinar de manera más precisa la causa de un error y seguir los pasos adecuados para la recuperación. Puede leer las propiedades del objeto **Error** para obtener detalles específicos sobre cada error, incluidas:</span><span class="sxs-lookup"><span data-stu-id="58046-p104">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover. You can read the **Error** object's properties to obtain specific details about each error, including:</span></span>

  - <span data-ttu-id="58046-119">La propiedad **[Description](error-description-property-dao.md)**, que contiene el texto de la alerta de error que se mostrará en la pantalla si no se captura el error.</span><span class="sxs-lookup"><span data-stu-id="58046-119">The **[Description](error-description-property-dao.md)** property, which contains the text of the error alert that will be displayed on the screen if the error is not trapped.</span></span>

  - <span data-ttu-id="58046-120">La propiedad **[Number](error-number-property-dao.md)**, que contiene el valor de tipo entero Long de la constante de error.</span><span class="sxs-lookup"><span data-stu-id="58046-120">The **[Number](error-number-property-dao.md)** property, which contains the Long integer value of the error constant.</span></span>

  - <span data-ttu-id="58046-p105">La propiedad **[Source](error-source-property-dao.md)**, que identifica el objeto que ha provocado el error. Esto es especialmente útil cuando tiene varios objetos **Error** en la colección **Errors** tras una solicitud de un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="58046-p105">The **[Source](error-source-property-dao.md)** property, which identifies the object that raised the error. This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to an ODBC data source.</span></span>

  - <span data-ttu-id="58046-123">Las propiedades **HelpFile** y **HelpContext**, que indican el archivo de Ayuda de Microsoft Windows y el tema de Ayuda adecuados, respectivamente, (si existen) para el error.</span><span class="sxs-lookup"><span data-stu-id="58046-123">The **HelpFile** and **HelpContext** properties, which indicate the appropriate Microsoft Windows Help file and Help topic, respectively, (if any exist) for the error.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="58046-124">[!NOTA] Al programar en Microsoft Visual Basic para Aplicaciones (VBA), si usa la palabra clave **New** para crear un objeto que provoca posteriormente un error antes de que se anexe este objeto a una colección, la colección **Errors** del objeto **DBEngine** no va a contener una entrada para este error del objeto porque el nuevo objeto no está asociado al objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="58046-124">When programming in Microsoft Visual Basic for Applications (VBA), if you use the **New** keyword to create an object that subsequently causes an error before that object has been appended to a collection, the **DBEngine** object's **Errors** collection won't contain an entry for that object's error, because the new object is not associated with the **DBEngine** object.</span></span> <span data-ttu-id="58046-125">No obstante, la información de error está disponible en el objeto **Err** VBA.</span><span class="sxs-lookup"><span data-stu-id="58046-125">However, the error information is available in the VBA **Err** object.</span></span> <span data-ttu-id="58046-126">El código de tratamiento de errores VBA debe examinar la colección **Errors** siempre que prevea un error de acceso a datos.</span><span class="sxs-lookup"><span data-stu-id="58046-126">Your VBA error-handling code should examine the **Errors** collection whenever you anticipate a data access error.</span></span> <span data-ttu-id="58046-127">Si está escribiendo un tratamiento de errores centralizado, compruebe el objeto **Err** VBA para determinar si la información de error de la colección **Errors** es válida.</span><span class="sxs-lookup"><span data-stu-id="58046-127">If you are writing a centralized error handler, test the VBA **Err** object to determine if the error information in the **Errors** collection is valid.</span></span> <span data-ttu-id="58046-128">Si la propiedad **Number** del último elemento de la colección **Errors** (DBEngine.Errors.Count - 1) y el valor del objeto **Err** coinciden, a continuación, puede usar una serie de instrucciones **Select Case** para identificar el error DAO determinado o errores que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="58046-128">If the **Number** property of the last element of the **Errors** collection (DBEngine.Errors.Count - 1) and the value of the **Err** object match, you can then use a series of **Select Case** statements to identify the particular DAO error or errors that occurred.</span></span> <span data-ttu-id="58046-129">Si no coinciden, use el método [Refresh](errors-refresh-method-dao.md) de la colección **Errors**.</span><span class="sxs-lookup"><span data-stu-id="58046-129">If they do not match, use the [Refresh](errors-refresh-method-dao.md) method on the **Errors** collection.</span></span>



## <a name="example"></a><span data-ttu-id="58046-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58046-130">Example</span></span>

<span data-ttu-id="58046-131">En este ejemplo se fuerza un error, se captura y se muestran las propiedades **Description**, **Number**, **Source**, **HelpContext** y **HelpFile** del objeto **Error** resultante.</span><span class="sxs-lookup"><span data-stu-id="58046-131">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

```vb 
Sub DescriptionX() 
 
   Dim dbsTest As Database 
 
   On Error GoTo ErrorHandler 
 
   ' Intentionally trigger an error. 
   Set dbsTest = OpenDatabase("NoDatabase") 
 
   Exit Sub 
 
ErrorHandler: 
   Dim strError As String 
   Dim errLoop As Error 
 
   ' Enumerate Errors collection and display properties of  
   ' each Error object. 
   For Each errLoop In Errors 
      With errLoop 
         strError = _ 
            "Error #" & .Number & vbCr 
         strError = strError & _ 
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```

