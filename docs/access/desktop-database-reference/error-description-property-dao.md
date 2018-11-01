---
title: Error.Description Property (DAO)
TOCTitle: Description Property
ms:assetid: 47a84bec-3258-f2c7-e1af-239da39844dc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193218(v=office.15)
ms:contentKeyID: 48544601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053358
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2de4c87832956fb690f67f734d418a855b179d8c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870341"
---
# <a name="errordescription-property-dao"></a><span data-ttu-id="f5a94-102">Error.Description Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="f5a94-102">Error.Description Property (DAO)</span></span>


<span data-ttu-id="f5a94-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5a94-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="f5a94-p101">Devuelve una cadena descriptiva asociada con un error. Ésta es la propiedad predeterminada del objeto **Error**.</span><span class="sxs-lookup"><span data-stu-id="f5a94-p101">Returns a descriptive string associated with an error. This is the default property for the **Error** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a94-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5a94-106">Syntax</span></span>

<span data-ttu-id="f5a94-107">*expresión* . Descripción</span><span class="sxs-lookup"><span data-stu-id="f5a94-107">*expression* .Description</span></span>

<span data-ttu-id="f5a94-108">*expresión* Variable que representa un objeto **Error** .</span><span class="sxs-lookup"><span data-stu-id="f5a94-108">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a94-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5a94-109">Remarks</span></span>

<span data-ttu-id="f5a94-p102">La propiedad **Description** incluye una descripción breve del error. Use esta propiedad para avisar al usuario acerca de un error que no puede o no desea controlar.</span><span class="sxs-lookup"><span data-stu-id="f5a94-p102">The **Description** property comprises a short description of the error. Use this property to alert the user about an error that you cannot or do not want to handle.</span></span>

## <a name="example"></a><span data-ttu-id="f5a94-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5a94-112">Example</span></span>

<span data-ttu-id="f5a94-113">En este ejemplo, se fuerza un error, se captura y se muestran las propiedades **Description**, **Number**, **Source**, **HelpContext** y **HelpFile** del objeto Error resultante.</span><span class="sxs-lookup"><span data-stu-id="f5a94-113">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting Error object.</span></span>

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

