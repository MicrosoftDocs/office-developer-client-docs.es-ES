---
title: Error.Source Property (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 16d043f1906744988af35708a954e9224256f8f7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867996"
---
# <a name="errorsource-property-dao"></a>Error.Source Property (DAO)


**Se aplica a**: Access 2013, Office 2013


Devuelve el nombre del objeto o de la aplicación que generó originalmente el error.

## <a name="syntax"></a>Sintaxis

*expresión* . Origen

*expresión* Variable que representa un objeto **Error** .

## <a name="remarks"></a>Observaciones

El valor de la propiedad **Source** suele ser el identificador de programa o el nombre de clase del objeto. Use la propiedad **Source** para proporcionar a los usuarios información cuando el código no puede controlar un error generado en un objeto en otra aplicación.

Por ejemplo, si para tener acceso a Microsoft Excel y se genera un error "División por cero", Microsoft Excel establece **Error.Number** en el código de Microsoft Excel correspondiente a dicho error y establece la propiedad **Source** en Excel.Application. Observe que si el error se genera en otro objeto invocado por Microsoft Excel, este intercepta el error y sigue estableciendo **Error.Number** en el código de Microsoft Excel. Sin embargo, las otras propiedades del objeto **Error** (incluida la propiedad **Source**) conservarán los valores establecidos por el objeto que generó el error. La propiedad **Source** siempre contiene el nombre del objeto que generó originalmente el error.

Basándose en toda la documentación del error, puede escribir código que controlará el error apropiadamente. Si el controlador de errores no actúa correctamente, puede usar la información del objeto **[Error](error-object-dao.md)** para describir el error al usuario, utilizando la propiedad **Source** y las demás propiedades de **Error** con el fin de proporcionar al usuario información sobre qué objeto generó originalmente el error, la descripción del mismo, etc.


> [!NOTE]
> La construcción **On Error Resume Next** puede ser preferible a **On Error GoTo** cuando se tratan errores generados durante el acceso a otros objetos. La comprobación de la propiedad del objeto **Error** después de cada interacción con un objeto elimina la ambigüedad sobre cuál fue el objeto al que obtuvo acceso el código cuando se produjo el error. De este modo, puede saber con seguridad qué objeto colocó el código de error en **Error.Number** y qué objeto generó originalmente el error (**Error.Source**).

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
     " " & .Description & vbCr 
     strError = strError & _ 
     " (Source: " & .Source & ")" & vbCr 
     strError = strError & _ 
     "Press F1 to see topic " & .HelpContext & vbCr 
     strError = strError & _ 
     " in the file " & .HelpFile & "." 
     End With 
     MsgBox strError 
     Next 
     
     Resume Next 
     
    End Sub
```
