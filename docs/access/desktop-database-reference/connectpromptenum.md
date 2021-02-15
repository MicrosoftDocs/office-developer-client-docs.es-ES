---
title: ConnectPromptEnum (referencia de base de datos de escritorio de Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295670"
---
# <a name="connectpromptenum"></a><span data-ttu-id="46764-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="46764-102">ConnectPromptEnum</span></span>

<span data-ttu-id="46764-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46764-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46764-104">Especifica si se debe mostrar un cuadro de diálogo para solicitar los parámetros que faltan al abrir una conexión con un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="46764-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46764-105">Constante</span><span class="sxs-lookup"><span data-stu-id="46764-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="46764-106">Valor</span><span class="sxs-lookup"><span data-stu-id="46764-106">Value</span></span></p></th>
<th><p><span data-ttu-id="46764-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="46764-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46764-108"><strong>adPromptAlways</strong></span><span class="sxs-lookup"><span data-stu-id="46764-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="46764-109">1 </span><span class="sxs-lookup"><span data-stu-id="46764-109">1</span></span></p></td>
<td><p><span data-ttu-id="46764-110">Solicita información siempre.</span><span class="sxs-lookup"><span data-stu-id="46764-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46764-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="46764-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="46764-112">2 </span><span class="sxs-lookup"><span data-stu-id="46764-112">2</span></span></p></td>
<td><p><span data-ttu-id="46764-113">Solicita más información si se necesita.</span><span class="sxs-lookup"><span data-stu-id="46764-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46764-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="46764-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="46764-115">3 </span><span class="sxs-lookup"><span data-stu-id="46764-115">3</span></span></p></td>
<td><p><span data-ttu-id="46764-116">Solicita más información si se necesita, pero no se admiten parámetros opcionales.</span><span class="sxs-lookup"><span data-stu-id="46764-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46764-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="46764-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="46764-118">4 </span><span class="sxs-lookup"><span data-stu-id="46764-118">4</span></span></p></td>
<td><p><span data-ttu-id="46764-119">No solicita información nunca.</span><span class="sxs-lookup"><span data-stu-id="46764-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="46764-120">Equivalente de ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="46764-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="46764-121">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="46764-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46764-122">Constante</span><span class="sxs-lookup"><span data-stu-id="46764-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46764-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="46764-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46764-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="46764-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46764-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="46764-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46764-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="46764-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

