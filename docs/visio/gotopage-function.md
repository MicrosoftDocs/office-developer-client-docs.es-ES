---
title: GOTOPAGE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Muestra la página que tiene el nombre pagename en la ventana activa actualmente.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302971"
---
# <a name="gotopage-function"></a><span data-ttu-id="c5036-103">Función GOTOPAGE</span><span class="sxs-lookup"><span data-stu-id="c5036-103">GOTOPAGE Function</span></span>

<span data-ttu-id="c5036-104">Muestra la página que tiene el nombre  *pagename*  en la ventana activa actualmente.</span><span class="sxs-lookup"><span data-stu-id="c5036-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c5036-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5036-105">Syntax</span></span>

<span data-ttu-id="c5036-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="c5036-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c5036-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5036-107">Parameters</span></span>

|<span data-ttu-id="c5036-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c5036-108">**Name**</span></span>|<span data-ttu-id="c5036-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c5036-109">**Required/Optional**</span></span>|<span data-ttu-id="c5036-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c5036-110">**Data Type**</span></span>|<span data-ttu-id="c5036-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5036-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c5036-112">_pagename_</span><span class="sxs-lookup"><span data-stu-id="c5036-112">_pagename_</span></span> <br/> |<span data-ttu-id="c5036-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c5036-113">Required</span></span>  <br/> |<span data-ttu-id="c5036-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c5036-114">**String**</span></span> <br/> |<span data-ttu-id="c5036-115">El nombre de la página a la que ir.</span><span class="sxs-lookup"><span data-stu-id="c5036-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5036-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5036-116">Remarks</span></span>

<span data-ttu-id="c5036-117">Si ya hay una ventana que muestra la página, se activa esa ventana.</span><span class="sxs-lookup"><span data-stu-id="c5036-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="c5036-118">Si  *pagename*  no existe, la aplicación intenta navegar hasta https://  *pagename*  /.</span><span class="sxs-lookup"><span data-stu-id="c5036-118">If  *pagename*  does not exist, the application attempts to navigate to https://  *pagename*  /.</span></span> <span data-ttu-id="c5036-119">Si Visio actúa como servidor local, la función GOTOPAGE no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="c5036-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="c5036-120">Puede utilizar la función HYPERLINK para buscar cualquier ruta de acceso DOS, UNC o dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c5036-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="c5036-p102">En versiones anteriores de Visio, esta función se denominaba _GOTOPAGE. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones.</span><span class="sxs-lookup"><span data-stu-id="c5036-p102">In earlier versions of Visio products, this function appears as _GOTOPAGE. Visio versions 4.0 and later accept either style.</span></span> 
  

