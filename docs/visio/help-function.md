---
title: HELP (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Abre un archivo de ayuda HTML con la palabra clave especificada en el cuadro Búsqueda.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431340"
---
# <a name="help-function"></a><span data-ttu-id="6b939-103">Función HELP</span><span class="sxs-lookup"><span data-stu-id="6b939-103">HELP Function</span></span>

<span data-ttu-id="6b939-104">Abre un archivo de ayuda HTML con la palabra  *clave*  especificada en el **cuadro** Búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6b939-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6b939-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b939-105">Syntax</span></span>

<span data-ttu-id="6b939-106">HELP(" \*\* *filename.chm!keyword* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="6b939-106">HELP(" \*\* *filename.chm!keyword* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6b939-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b939-107">Parameters</span></span>

|<span data-ttu-id="6b939-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6b939-108">**Name**</span></span>|<span data-ttu-id="6b939-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="6b939-109">**Required/Optional**</span></span>|<span data-ttu-id="6b939-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="6b939-110">**Data Type**</span></span>|<span data-ttu-id="6b939-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b939-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6b939-112">_filename.chm!keyword_</span><span class="sxs-lookup"><span data-stu-id="6b939-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="6b939-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6b939-113">Required</span></span>  <br/> |<span data-ttu-id="6b939-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6b939-114">**String**</span></span> <br/> | <span data-ttu-id="6b939-115">El nombre del archivo de Ayuda y la palabra clave para buscar.</span><span class="sxs-lookup"><span data-stu-id="6b939-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b939-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b939-116">Remarks</span></span>

<span data-ttu-id="6b939-117">Si no  *se especifica*  ninguna palabra clave, la función HELP abre la página de contenido del archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="6b939-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6b939-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b939-118">Example</span></span>

<span data-ttu-id="6b939-119">HELP("visio.chm!shapesheet")</span><span class="sxs-lookup"><span data-stu-id="6b939-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="6b939-120">Abre el archivo de Ayuda de Visio y muestra una lista de temas cuyas palabra clave es "forma".</span><span class="sxs-lookup"><span data-stu-id="6b939-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

