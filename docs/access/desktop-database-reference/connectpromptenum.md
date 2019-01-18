---
title: ConnectPromptEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701112"
---
# <a name="connectpromptenum"></a><span data-ttu-id="d0891-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="d0891-102">ConnectPromptEnum</span></span>

<span data-ttu-id="d0891-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0891-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0891-104">Especifica si se debe mostrar un cuadro de diálogo para solicitar los parámetros que faltan al abrir una conexión con un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="d0891-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0891-105">Constante</span><span class="sxs-lookup"><span data-stu-id="d0891-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d0891-106">Valor</span><span class="sxs-lookup"><span data-stu-id="d0891-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d0891-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0891-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0891-108"><strong>adPromptAlways</strong></span><span class="sxs-lookup"><span data-stu-id="d0891-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="d0891-109">1</span><span class="sxs-lookup"><span data-stu-id="d0891-109">1</span></span></p></td>
<td><p><span data-ttu-id="d0891-110">Solicita información siempre.</span><span class="sxs-lookup"><span data-stu-id="d0891-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0891-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="d0891-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="d0891-112">2</span><span class="sxs-lookup"><span data-stu-id="d0891-112">2</span></span></p></td>
<td><p><span data-ttu-id="d0891-113">Solicita más información si se necesita.</span><span class="sxs-lookup"><span data-stu-id="d0891-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0891-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="d0891-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="d0891-115">3</span><span class="sxs-lookup"><span data-stu-id="d0891-115">3</span></span></p></td>
<td><p><span data-ttu-id="d0891-116">Solicita más información si se necesita, pero no se admiten parámetros opcionales.</span><span class="sxs-lookup"><span data-stu-id="d0891-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0891-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="d0891-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="d0891-118">4</span><span class="sxs-lookup"><span data-stu-id="d0891-118">4</span></span></p></td>
<td><p><span data-ttu-id="d0891-119">No solicita información nunca.</span><span class="sxs-lookup"><span data-stu-id="d0891-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d0891-120">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d0891-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="d0891-121">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="d0891-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0891-122">Constante</span><span class="sxs-lookup"><span data-stu-id="d0891-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0891-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="d0891-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0891-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="d0891-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0891-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="d0891-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0891-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="d0891-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

