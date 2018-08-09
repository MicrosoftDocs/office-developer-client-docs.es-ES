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
description: Muestra la página que tiene el nombre pagename en la ventana actualmente activa.
ms.openlocfilehash: 67f8a79b854fd6f2ae47e39877ffcdbe4a1be5cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822248"
---
# <a name="gotopage-function"></a><span data-ttu-id="ab6df-103">Función GOTOPAGE</span><span class="sxs-lookup"><span data-stu-id="ab6df-103">GOTOPAGE Function</span></span>

<span data-ttu-id="ab6df-104">Muestra la página que tiene el nombre *pagename* en la ventana actualmente activa.</span><span class="sxs-lookup"><span data-stu-id="ab6df-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ab6df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab6df-105">Syntax</span></span>

<span data-ttu-id="ab6df-106">GOTOPAGE ("** *pagename* **")</span><span class="sxs-lookup"><span data-stu-id="ab6df-106">GOTOPAGE(" ** *pagename* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ab6df-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab6df-107">Parameters</span></span>

|<span data-ttu-id="ab6df-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ab6df-108">**Name**</span></span>|<span data-ttu-id="ab6df-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="ab6df-109">**Required/Optional**</span></span>|<span data-ttu-id="ab6df-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ab6df-110">**Data Type**</span></span>|<span data-ttu-id="ab6df-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab6df-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ab6df-112">_pagename_</span><span class="sxs-lookup"><span data-stu-id="ab6df-112">_pagename_</span></span> <br/> |<span data-ttu-id="ab6df-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ab6df-113">Required</span></span>  <br/> |<span data-ttu-id="ab6df-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ab6df-114">**String**</span></span> <br/> |<span data-ttu-id="ab6df-115">El nombre de la página a la que ir.</span><span class="sxs-lookup"><span data-stu-id="ab6df-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab6df-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab6df-116">Remarks</span></span>

<span data-ttu-id="ab6df-117">Si una ventana ya muestra la página, esa ventana se convierte en activa.</span><span class="sxs-lookup"><span data-stu-id="ab6df-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="ab6df-118">Si *pagename* no existe, la aplicación intenta vaya a http:// *pagename* /.</span><span class="sxs-lookup"><span data-stu-id="ab6df-118">If  *pagename*  does not exist, the application attempts to navigate to http://  *pagename*  /.</span></span> <span data-ttu-id="ab6df-119">Si Visio actúa como un servidor en contexto, la función GOTOPAGE tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="ab6df-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="ab6df-120">Puede utilizar la función HYPERLINK para buscar cualquier ruta de acceso DOS, UNC o dirección URL.</span><span class="sxs-lookup"><span data-stu-id="ab6df-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="ab6df-p102">En versiones anteriores de Visio, esta función se denominaba _GOTOPAGE. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones.</span><span class="sxs-lookup"><span data-stu-id="ab6df-p102">In earlier versions of Visio products, this function appears as _GOTOPAGE. Visio versions 4.0 and later accept either style.</span></span> 
  

