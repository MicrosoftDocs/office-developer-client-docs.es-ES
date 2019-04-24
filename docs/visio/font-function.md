---
title: Función FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Devuelve el valor entero del identificador único de una fuente, especificado por su nombre.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346140"
---
# <a name="font-function"></a><span data-ttu-id="321ab-103">Función FONT</span><span class="sxs-lookup"><span data-stu-id="321ab-103">FONT Function</span></span>

<span data-ttu-id="321ab-104">Devuelve el valor entero del identificador único de una fuente, especificado por su nombre.</span><span class="sxs-lookup"><span data-stu-id="321ab-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="321ab-105">En la mayoría de los casos, el identificador de fuente es específico del sistema.</span><span class="sxs-lookup"><span data-stu-id="321ab-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="321ab-106">Aunque la fuente permanece establecida una vez utilizada en un archivo, la función **Font** proporciona un acceso coherente a una fuente en particular en sistemas y versiones de Visio.</span><span class="sxs-lookup"><span data-stu-id="321ab-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="321ab-107">Se recomienda usar la función **Font** para asignar fuentes en lugar de hacer referencia a identificadores de fuente directamente.</span><span class="sxs-lookup"><span data-stu-id="321ab-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="321ab-108">Información de versiones</span><span class="sxs-lookup"><span data-stu-id="321ab-108">Version Information</span></span>

<span data-ttu-id="321ab-109">Versión añadida: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="321ab-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="321ab-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="321ab-110">Syntax</span></span>

 <span data-ttu-id="321ab-111">**Fuente** ( _"font_name_string"_)</span><span class="sxs-lookup"><span data-stu-id="321ab-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="321ab-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="321ab-112">Parameters</span></span>

|<span data-ttu-id="321ab-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="321ab-113">**Name**</span></span>|<span data-ttu-id="321ab-114">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="321ab-114">**Required/Optional**</span></span>|<span data-ttu-id="321ab-115">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="321ab-115">**Data Type**</span></span>|<span data-ttu-id="321ab-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="321ab-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="321ab-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="321ab-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="321ab-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="321ab-118">Required</span></span>  <br/> |<span data-ttu-id="321ab-119">**string**</span><span class="sxs-lookup"><span data-stu-id="321ab-119">**string**</span></span> <br/> |<span data-ttu-id="321ab-120">Nombre de la fuente.</span><span class="sxs-lookup"><span data-stu-id="321ab-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="321ab-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="321ab-121">Return value</span></span>

<span data-ttu-id="321ab-122">Entero</span><span class="sxs-lookup"><span data-stu-id="321ab-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="321ab-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="321ab-123">Remarks</span></span>

<span data-ttu-id="321ab-124">Si la cadena proporcionada para *font_name_string* no coincide con una fuente conocida, esta función devuelve un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="321ab-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="321ab-125">error.</span><span class="sxs-lookup"><span data-stu-id="321ab-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="321ab-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="321ab-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="321ab-127">Devuelve el valor entero (4) que representa el identificador único para la fuente "caLibri".</span><span class="sxs-lookup"><span data-stu-id="321ab-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

