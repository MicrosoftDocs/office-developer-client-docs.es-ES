---
title: DOCMD (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Ejecuta el comando identificado.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413076"
---
# <a name="docmd-function"></a><span data-ttu-id="509b3-103">Función DOCMD</span><span class="sxs-lookup"><span data-stu-id="509b3-103">DOCMD Function</span></span>

<span data-ttu-id="509b3-104">Ejecuta el comando identificado.</span><span class="sxs-lookup"><span data-stu-id="509b3-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="509b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="509b3-105">Syntax</span></span>

 <span data-ttu-id="509b3-106">**DoCmd** ( __ CommandID)</span><span class="sxs-lookup"><span data-stu-id="509b3-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="509b3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="509b3-107">Parameters</span></span>

|<span data-ttu-id="509b3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="509b3-108">**Name**</span></span>|<span data-ttu-id="509b3-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="509b3-109">**Required/Optional**</span></span>|<span data-ttu-id="509b3-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="509b3-110">**Data Type**</span></span>|<span data-ttu-id="509b3-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="509b3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="509b3-112">_commandId_</span><span class="sxs-lookup"><span data-stu-id="509b3-112">_commandID_</span></span> <br/> |<span data-ttu-id="509b3-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="509b3-113">Required</span></span>  <br/> |<span data-ttu-id="509b3-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="509b3-114">**Number**</span></span> <br/> | <span data-ttu-id="509b3-115">Comando que se debe ejecutar.</span><span class="sxs-lookup"><span data-stu-id="509b3-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="509b3-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="509b3-116">Remarks</span></span>

<span data-ttu-id="509b3-117">Para obtener una lista de los comandos compatibles con la función DOCMD, vea el tema "comandos DoCmd/DOCMD" en la referencia de automatización de Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="509b3-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="509b3-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="509b3-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="509b3-119">Hace que el cuadro de diálogo **Datos de formas** aparezca en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="509b3-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

