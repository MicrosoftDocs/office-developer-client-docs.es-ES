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
ms.openlocfilehash: e425dd9605c18d4647787c5df7aeaa4fd5f9e4cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821999"
---
# <a name="docmd-function"></a><span data-ttu-id="a3b9b-103">Función DOCMD</span><span class="sxs-lookup"><span data-stu-id="a3b9b-103">DOCMD Function</span></span>

<span data-ttu-id="a3b9b-104">Ejecuta el comando identificado.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a3b9b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3b9b-105">Syntax</span></span>

 <span data-ttu-id="a3b9b-106">**DOCMD** ( _IDcomando_)</span><span class="sxs-lookup"><span data-stu-id="a3b9b-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="a3b9b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3b9b-107">Parameters</span></span>

|<span data-ttu-id="a3b9b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a3b9b-108">**Name**</span></span>|<span data-ttu-id="a3b9b-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="a3b9b-109">**Required/Optional**</span></span>|<span data-ttu-id="a3b9b-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a3b9b-110">**Data Type**</span></span>|<span data-ttu-id="a3b9b-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3b9b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a3b9b-112">_IDcomando_</span><span class="sxs-lookup"><span data-stu-id="a3b9b-112">_commandID_</span></span> <br/> |<span data-ttu-id="a3b9b-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a3b9b-113">Required</span></span>  <br/> |<span data-ttu-id="a3b9b-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="a3b9b-114">**Number**</span></span> <br/> | <span data-ttu-id="a3b9b-115">Comando que se debe ejecutar.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3b9b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3b9b-116">Remarks</span></span>

<span data-ttu-id="a3b9b-117">Para obtener una lista de comandos que son compatibles con la función DOCMD, vea el tema "Comandos DoCmd/DOCMD" en la referencia de automatización de Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a3b9b-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3b9b-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="a3b9b-119">Hace que el cuadro de diálogo **Datos de formas** aparezca en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

