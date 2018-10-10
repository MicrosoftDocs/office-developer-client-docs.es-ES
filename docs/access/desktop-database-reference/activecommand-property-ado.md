---
title: ActiveCommand (propiedad, ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486204"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="98f85-102">ActiveCommand (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="98f85-102">ActiveCommand Property (ADO)</span></span>


<span data-ttu-id="98f85-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98f85-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="98f85-104">Indica el objeto [Command](command-object-ado.md) que ha creado el objeto [Recordset](recordset-object-ado.md) asociado.</span><span class="sxs-lookup"><span data-stu-id="98f85-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="98f85-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98f85-105">Return Value</span></span>

<span data-ttu-id="98f85-p101">Devuelve un valor de tipo **Variant** que contiene un objeto **Command**. El valor predeterminado es una referencia de objeto nula.</span><span class="sxs-lookup"><span data-stu-id="98f85-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="98f85-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98f85-108">Remarks</span></span>

<span data-ttu-id="98f85-109">La propiedad **ActiveCommand** es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="98f85-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="98f85-110">Si no se usó un objeto **Command** para crear el objeto **Recordset** actual, se devuelve una referencia de objeto **Null**.</span><span class="sxs-lookup"><span data-stu-id="98f85-110">If a **Command** object was not used to create the current **Recordset**, then a **Null** object reference is returned.</span></span>

<span data-ttu-id="98f85-111">Use esta propiedad para buscar el objeto **Command** asociado cuando solo dispone del objeto **Recordset** resultante.</span><span class="sxs-lookup"><span data-stu-id="98f85-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

