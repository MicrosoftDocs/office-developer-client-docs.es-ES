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
# <a name="errornumber-property-dao"></a><span data-ttu-id="52350-102">Propiedad Error.Number (DAO)</span><span class="sxs-lookup"><span data-stu-id="52350-102">Error.Number property (DAO)</span></span>


<span data-ttu-id="52350-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52350-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="52350-104">Devuelve un valor numérico que especifica un error.</span><span class="sxs-lookup"><span data-stu-id="52350-104">Returns a numeric value specifying an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="52350-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52350-105">Syntax</span></span>

<span data-ttu-id="52350-106">*expresión* . Número</span><span class="sxs-lookup"><span data-stu-id="52350-106">*expression* .Number</span></span>

<span data-ttu-id="52350-107">*expresión* Variable que representa un objeto **Error** .</span><span class="sxs-lookup"><span data-stu-id="52350-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="52350-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52350-108">Remarks</span></span>

<span data-ttu-id="52350-p101">Utilice la propiedad **Number** para determinar el error producido. El valor de la propiedad se corresponde con un número de captura exclusivo que a su vez se corresponde con una condición de error.</span><span class="sxs-lookup"><span data-stu-id="52350-p101">Use the **Number** property to determine the error that occurred. The value of the property corresponds to a unique trap number that corresponds to an error condition.</span></span>

## <a name="example"></a><span data-ttu-id="52350-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52350-111">Example</span></span>

<span data-ttu-id="52350-112">En este ejemplo se fuerza un error, se captura y se muestran las propiedades **Description**, **Number**, **Source**, **HelpContext** y **HelpFile** del objeto **Error** resultante.</span><span class="sxs-lookup"><span data-stu-id="52350-112">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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

