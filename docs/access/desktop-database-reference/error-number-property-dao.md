---
title: Propiedad Error.Number (DAO)
TOCTitle: Number Property
ms:assetid: 2fb94dca-f990-04f8-bbd2-9919d28de75a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192259(v=office.15)
ms:contentKeyID: 48544013
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053363
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 95d814bb613b848f65b61cd342d2918fbbd2fea2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928345"
---
# <a name="errornumber-property-dao"></a>Propiedad Error.Number (DAO)


**Se aplica a**: Access 2013, Office 2013
 

Devuelve un valor numérico que especifica un error.

## <a name="syntax"></a>Sintaxis

*expresión* . Número

*expresión* Variable que representa un objeto **Error** .

## <a name="remarks"></a>Observaciones

Utilice la propiedad **Number** para determinar el error producido. El valor de la propiedad se corresponde con un número de captura exclusivo que a su vez se corresponde con una condición de error.

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

