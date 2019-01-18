---
title: ActiveCommand (propiedad, ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705298"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="e04e8-102">ActiveCommand (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="e04e8-102">ActiveCommand property (ADO)</span></span>

<span data-ttu-id="e04e8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e04e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e04e8-104">Indica el objeto [Command](command-object-ado.md) que ha creado el objeto [Recordset](recordset-object-ado.md) asociado.</span><span class="sxs-lookup"><span data-stu-id="e04e8-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="e04e8-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e04e8-105">Return value</span></span>

<span data-ttu-id="e04e8-p101">Devuelve un valor de tipo **Variant** que contiene un objeto **Command**. El valor predeterminado es una referencia de objeto nula.</span><span class="sxs-lookup"><span data-stu-id="e04e8-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="e04e8-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e04e8-108">Remarks</span></span>

<span data-ttu-id="e04e8-109">La propiedad **ActiveCommand** es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e04e8-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="e04e8-110">Si un objeto **Command** no se usó para crear el **objeto Recordset**actual, se devuelve una referencia de objeto **Null** .</span><span class="sxs-lookup"><span data-stu-id="e04e8-110">If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>

<span data-ttu-id="e04e8-111">Use esta propiedad para buscar el objeto **Command** asociado cuando solo dispone del objeto **Recordset** resultante.</span><span class="sxs-lookup"><span data-stu-id="e04e8-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

