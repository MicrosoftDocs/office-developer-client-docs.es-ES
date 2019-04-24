---
title: FIELDPICTURE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Devuelve una cadena de formato de imagen que coincide con el código de formato interno del campo de texto de Microsoft Visio.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322550"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="1e8fa-103">Función FIELDPICTURE</span><span class="sxs-lookup"><span data-stu-id="1e8fa-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="1e8fa-104">Devuelve una cadena de formato de imagen que coincide con el código de formato interno del campo de texto de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="1e8fa-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1e8fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e8fa-105">Syntax</span></span>

<span data-ttu-id="1e8fa-106">FIELDPICTURE (\* \* *código* \* \*)</span><span class="sxs-lookup"><span data-stu-id="1e8fa-106">FIELDPICTURE(\*\* *code* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1e8fa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e8fa-107">Parameters</span></span>

|<span data-ttu-id="1e8fa-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1e8fa-108">**Name**</span></span>|<span data-ttu-id="1e8fa-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="1e8fa-109">**Required/Optional**</span></span>|<span data-ttu-id="1e8fa-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="1e8fa-110">**Data Type**</span></span>|<span data-ttu-id="1e8fa-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1e8fa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1e8fa-112">_code_</span><span class="sxs-lookup"><span data-stu-id="1e8fa-112">_code_</span></span> <br/> |<span data-ttu-id="1e8fa-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1e8fa-113">Required</span></span>  <br/> |<span data-ttu-id="1e8fa-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="1e8fa-114">**Number**</span></span> <br/> | <span data-ttu-id="1e8fa-115">Un código de formato de campo de texto.</span><span class="sxs-lookup"><span data-stu-id="1e8fa-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1e8fa-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e8fa-116">Return value</span></span>

<span data-ttu-id="1e8fa-117">String</span><span class="sxs-lookup"><span data-stu-id="1e8fa-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1e8fa-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e8fa-118">Remarks</span></span>

<span data-ttu-id="1e8fa-119">Las cadenas de formato de imagen se utilizan en la función FORMAT para definir la forma de realizar la ampliación de valores para convertirlos en fechas, horas, números y etiquetas de unidades.</span><span class="sxs-lookup"><span data-stu-id="1e8fa-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="1e8fa-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e8fa-120">Example</span></span>

<span data-ttu-id="1e8fa-121">FIELDPICTURE (0)</span><span class="sxs-lookup"><span data-stu-id="1e8fa-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="1e8fa-122">Devuelve la cadena de formato de imagen "esc(0)", que especifica un número con un decimal y la descripción de las unidades en letras minúsculas cuando se usa en la función FORMAT.</span><span class="sxs-lookup"><span data-stu-id="1e8fa-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

