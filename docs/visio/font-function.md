---
title: Función FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Devuelve el valor entero del identificador único para una fuente, especificado por nombre.
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822181"
---
# <a name="font-function"></a><span data-ttu-id="e90e0-103">Función FONT</span><span class="sxs-lookup"><span data-stu-id="e90e0-103">FONT Function</span></span>

<span data-ttu-id="e90e0-104">Devuelve el valor entero del identificador único para una fuente, especificado por nombre.</span><span class="sxs-lookup"><span data-stu-id="e90e0-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e90e0-105">En la mayoría de los casos, el identificador de la fuente es específico del sistema.</span><span class="sxs-lookup"><span data-stu-id="e90e0-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="e90e0-106">Aunque la fuente permanece establecida una vez utilizado en un archivo, la función de **fuente** proporciona acceso coherente a una fuente en particular a través de sistemas y versiones de Visio.</span><span class="sxs-lookup"><span data-stu-id="e90e0-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="e90e0-107">Se recomienda que utilice la función de la **fuente** para asignar a las fuentes en lugar de hacer referencia a los identificadores de fuente directamente.</span><span class="sxs-lookup"><span data-stu-id="e90e0-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="e90e0-108">Información de versión</span><span class="sxs-lookup"><span data-stu-id="e90e0-108">Version Information</span></span>

<span data-ttu-id="e90e0-109">Versión añadida: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="e90e0-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e90e0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e90e0-110">Syntax</span></span>

 <span data-ttu-id="e90e0-111">**Fuente** ( _"font_name_string"_)</span><span class="sxs-lookup"><span data-stu-id="e90e0-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="e90e0-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e90e0-112">Parameters</span></span>

|<span data-ttu-id="e90e0-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="e90e0-113">**Name**</span></span>|<span data-ttu-id="e90e0-114">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="e90e0-114">**Required/Optional**</span></span>|<span data-ttu-id="e90e0-115">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="e90e0-115">**Data Type**</span></span>|<span data-ttu-id="e90e0-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e90e0-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e90e0-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="e90e0-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="e90e0-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e90e0-118">Required</span></span>  <br/> |<span data-ttu-id="e90e0-119">**string**</span><span class="sxs-lookup"><span data-stu-id="e90e0-119">**string**</span></span> <br/> |<span data-ttu-id="e90e0-120">Nombre de la fuente.</span><span class="sxs-lookup"><span data-stu-id="e90e0-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="e90e0-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e90e0-121">Return value</span></span>

<span data-ttu-id="e90e0-122">Entero</span><span class="sxs-lookup"><span data-stu-id="e90e0-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e90e0-123">Notas</span><span class="sxs-lookup"><span data-stu-id="e90e0-123">Remarks</span></span>

<span data-ttu-id="e90e0-124">Si la cadena proporcionada para *font_name_string* no coincide con una fuente conocida, esta función devuelve #VALUE!</span><span class="sxs-lookup"><span data-stu-id="e90e0-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="e90e0-125">error.</span><span class="sxs-lookup"><span data-stu-id="e90e0-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e90e0-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e90e0-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="e90e0-127">Devuelve el valor de entero (4) que representa el identificador exclusivo para la fuente "Calibri".</span><span class="sxs-lookup"><span data-stu-id="e90e0-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

