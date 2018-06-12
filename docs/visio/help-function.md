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
description: Abre un archivo de Ayuda HTML con la palabra clave de especificadas en el cuadro de búsqueda.
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822276"
---
# <a name="help-function"></a><span data-ttu-id="ab725-103">HELP (función)</span><span class="sxs-lookup"><span data-stu-id="ab725-103">HELP Function</span></span>

<span data-ttu-id="ab725-104">Abre un archivo de Ayuda HTML con la *palabra clave* palabra especificadas en el cuadro de **búsqueda** .</span><span class="sxs-lookup"><span data-stu-id="ab725-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ab725-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab725-105">Syntax</span></span>

<span data-ttu-id="ab725-106">Ayuda ("** *filename.chm!keyword* **")</span><span class="sxs-lookup"><span data-stu-id="ab725-106">HELP(" ** *filename.chm!keyword* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ab725-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab725-107">Parameters</span></span>

|<span data-ttu-id="ab725-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ab725-108">**Name**</span></span>|<span data-ttu-id="ab725-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="ab725-109">**Required/Optional**</span></span>|<span data-ttu-id="ab725-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ab725-110">**Data Type**</span></span>|<span data-ttu-id="ab725-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab725-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ab725-112">_FileName.chm!Keyword_</span><span class="sxs-lookup"><span data-stu-id="ab725-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="ab725-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ab725-113">Required</span></span>  <br/> |<span data-ttu-id="ab725-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ab725-114">**String**</span></span> <br/> | <span data-ttu-id="ab725-115">El nombre del archivo de Ayuda y la palabra clave para buscar.</span><span class="sxs-lookup"><span data-stu-id="ab725-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab725-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab725-116">Remarks</span></span>

<span data-ttu-id="ab725-117">Si no se especifica ninguna *palabra clave* , la función HELP abre la página de contenido del archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="ab725-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ab725-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab725-118">Example</span></span>

<span data-ttu-id="ab725-119">Help("Visio.chm!ShapeSheet")</span><span class="sxs-lookup"><span data-stu-id="ab725-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="ab725-120">Abre el archivo de Ayuda de Visio y muestra una lista de temas cuyas palabra clave es "forma".</span><span class="sxs-lookup"><span data-stu-id="ab725-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

