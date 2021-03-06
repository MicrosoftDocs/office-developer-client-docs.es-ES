---
title: Propiedad Error.Source (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 79c5fa1e01bbb6bce4f2cef705f23f3259bf0678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293444"
---
# <a name="errorsource-property-dao"></a>Propiedad Error.Source (DAO)


**Se aplica a:** Access 2013, Office 2013


Devuelve el nombre del objeto o de la aplicación que generó originalmente el error.

## <a name="syntax"></a>Sintaxis

*expresión* . Origen

*expresión* Variable que representa un **objeto Error.**

## <a name="remarks"></a>Comentarios

El valor de la propiedad **Source** suele ser el identificador de programa o el nombre de clase del objeto. Use la propiedad **Source** para proporcionar a los usuarios información cuando el código no puede controlar un error generado en un objeto en otra aplicación.

Por ejemplo, si tiene acceso a Microsoft Excel y genera un error de "División por cero", Microsoft Excel establece **Error.Number** en el código Microsoft Excel para dicho error y establece la **propiedad Source** en Excel. Aplicación. Observe que si el error se genera en otro objeto invocado por Microsoft Excel, este intercepta el error y sigue estableciendo **Error.Number** en el código de Microsoft Excel. Sin embargo, las otras propiedades del objeto **Error** (incluida la propiedad **Source**) conservarán los valores establecidos por el objeto que generó el error. La propiedad **Source** siempre contiene el nombre del objeto que generó originalmente el error.

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
