---
title: 'Objetos de objeto de error: acceso a datos (DAO)'
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62b195907d5acc05832c1feac45165aadd9e14d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484643"
---
# <a name="error-object-dao"></a>Error Object (DAO)


**Se aplica a**: Access 2013 | Office 2013

El objeto **Error** contiene detalles sobre los errores de acceso a datos, cada uno de los cuales pertenece a una operación única que implica a DAO.

## <a name="remarks"></a>Observaciones

Cualquier operación que implica a DAO puede generar uno o varios errores. Por ejemplo, una llamada a un servidor ODBC puede provocar un error del servidor de base de datos, un error de ODBC o de DAO. Cuando se produce uno de estos errores, se coloca un objeto **Error** en la colección **Errors** del objeto **DBEngine**. Un único evento puede provocar, por lo tanto, varios objetos **Error** que aparecen en la colección **Errors**.

Cuando una operación DAO posterior genera un error, se borra la colección **Errors** y uno o varios objetos nuevos **Error** se colocan en la colección **Errors**. Las operaciones DAO que no generan errores no tienen efecto en la colección **Errors**.

El conjunto de objetos **Error** en la colección **Errors** describe un único error. El primer objeto **Error** es el error de nivel más bajo (el error de origen), el segundo, el error de nivel inmediatamente superior, etc. Por ejemplo, si se produce un error de ODBC mientras intenta abrir un objeto **[Recordset](recordset-object-dao.md)**, el primer objeto **Error**  **Errors**(0) contiene el nivel de error de ODBC más bajo; los errores posteriores contienen los errores de ODBC devueltos por las distintas capas de ODBC. En este caso, el administrador de controladores ODBC, y posiblemente el controlador mismo, devuelven objetos **Error** separados. El último objeto **Error**  **Errors.Count-** 1 contiene el error de DAO que indica que no se pudo abrir el objeto.

Enumerar los errores específicos en la colección **Errors** permite rutinas de tratamiento de errores para determinar de manera más precisa la causa de un error y seguir los pasos adecuados para la recuperación. Puede leer las propiedades del objeto **Error** para obtener detalles específicos sobre cada error, incluidas:

  - La propiedad **[Description](error-description-property-dao.md)**, que contiene el texto de la alerta de error que se mostrará en la pantalla si no se captura el error.

  - La propiedad **[Number](error-number-property-dao.md)**, que contiene el valor de tipo entero Long de la constante de error.

  - La propiedad **[Source](error-source-property-dao.md)**, que identifica el objeto que ha provocado el error. Esto es especialmente útil cuando tiene varios objetos **Error** en la colección **Errors** tras una solicitud de un origen de datos ODBC.

  - Las propiedades **HelpFile** y **HelpContext**, que indican el archivo de Ayuda de Microsoft Windows y el tema de Ayuda adecuados, respectivamente, (si existen) para el error.
    

    > [!NOTE]
    > <P>[!NOTA] Al programar en Microsoft Visual Basic para Aplicaciones (VBA), si usa la palabra clave <STRONG>New</STRONG> para crear un objeto que provoca posteriormente un error antes de que se anexe este objeto a una colección, la colección <STRONG>Errors</STRONG> del objeto <STRONG>DBEngine</STRONG> no va a contener una entrada para este error del objeto porque el nuevo objeto no está asociado al objeto <STRONG>DBEngine</STRONG>. No obstante, la información de error está disponible en el objeto <STRONG>Err</STRONG> VBA. El código de tratamiento de errores VBA debe examinar la colección <STRONG>Errors</STRONG> siempre que prevea un error de acceso a datos. Si está escribiendo un tratamiento de errores centralizado, compruebe el objeto <STRONG>Err</STRONG> VBA para determinar si la información de error de la colección <STRONG>Errors</STRONG> es válida. Si la propiedad <STRONG>Number</STRONG> del último elemento de la colección <STRONG>Errors</STRONG> (DBEngine.Errors.Count - 1) y el valor del objeto <STRONG>Err</STRONG> coinciden, a continuación, puede usar una serie de instrucciones <STRONG>Select Case</STRONG> para identificar el error DAO determinado o errores que se ha producido. Si no coinciden, use el método <STRONG><A href="errors-refresh-method-dao.md">Refresh</A></STRONG> de la colección <STRONG>Errors</STRONG>.</P>



## <a name="example"></a>Ejemplo

En este ejemplo se fuerza un error, se captura y se muestran las propiedades **Description**, **Number**, **Source**, **HelpContext** y **HelpFile** del objeto **Error** resultante.

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

