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
description: Devuelve una cadena de formato de imagen que coincide con el código de formato Visio campo de texto interno de Microsoft.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431459"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="8c080-103">Función FIELDPICTURE</span><span class="sxs-lookup"><span data-stu-id="8c080-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="8c080-104">Devuelve una cadena de formato de imagen que coincide con el código de formato Visio campo de texto interno de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8c080-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8c080-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c080-105">Syntax</span></span>

<span data-ttu-id="8c080-106">FIELDPICTURE(\*\* *code* \*\* )</span><span class="sxs-lookup"><span data-stu-id="8c080-106">FIELDPICTURE(\*\* *code* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8c080-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c080-107">Parameters</span></span>

|<span data-ttu-id="8c080-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8c080-108">**Name**</span></span>|<span data-ttu-id="8c080-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="8c080-109">**Required/Optional**</span></span>|<span data-ttu-id="8c080-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="8c080-110">**Data Type**</span></span>|<span data-ttu-id="8c080-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c080-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8c080-112">_code_</span><span class="sxs-lookup"><span data-stu-id="8c080-112">_code_</span></span> <br/> |<span data-ttu-id="8c080-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8c080-113">Required</span></span>  <br/> |<span data-ttu-id="8c080-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="8c080-114">**Number**</span></span> <br/> | <span data-ttu-id="8c080-115">Un código de formato de campo de texto.</span><span class="sxs-lookup"><span data-stu-id="8c080-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8c080-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c080-116">Return value</span></span>

<span data-ttu-id="8c080-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="8c080-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c080-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c080-118">Remarks</span></span>

<span data-ttu-id="8c080-119">Las cadenas de formato de imagen se utilizan en la función FORMAT para definir la forma de realizar la ampliación de valores para convertirlos en fechas, horas, números y etiquetas de unidades.</span><span class="sxs-lookup"><span data-stu-id="8c080-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="8c080-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c080-120">Example</span></span>

<span data-ttu-id="8c080-121">FIELDPICTURE(0)</span><span class="sxs-lookup"><span data-stu-id="8c080-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="8c080-122">Devuelve la cadena de formato de imagen "esc(0)", que especifica un número con un decimal y la descripción de las unidades en letras minúsculas cuando se usa en la función FORMAT.</span><span class="sxs-lookup"><span data-stu-id="8c080-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

