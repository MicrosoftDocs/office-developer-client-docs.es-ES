---
title: UNICHAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Devuelve el carácter Unicode de un número.
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823481"
---
# <a name="unichar-function"></a><span data-ttu-id="28a50-103">UNICHAR (función)</span><span class="sxs-lookup"><span data-stu-id="28a50-103">UNICHAR Function</span></span>

<span data-ttu-id="28a50-104">Devuelve el carácter Unicode de un número.</span><span class="sxs-lookup"><span data-stu-id="28a50-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="28a50-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28a50-105">Syntax</span></span>

<span data-ttu-id="28a50-106">UNICHAR (** *número* **)</span><span class="sxs-lookup"><span data-stu-id="28a50-106">UNICHAR (** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="28a50-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28a50-107">Parameters</span></span>

|<span data-ttu-id="28a50-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="28a50-108">**Name**</span></span>|<span data-ttu-id="28a50-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="28a50-109">**Required/Optional**</span></span>|<span data-ttu-id="28a50-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="28a50-110">**Data Type**</span></span>|<span data-ttu-id="28a50-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28a50-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28a50-112">_number_</span><span class="sxs-lookup"><span data-stu-id="28a50-112">_number_</span></span> <br/> |<span data-ttu-id="28a50-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="28a50-113">Required</span></span>  <br/> |<span data-ttu-id="28a50-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="28a50-114">**Integer**</span></span> <br/> |<span data-ttu-id="28a50-115">Debe ser un entero comprendido entre 1 y 65.535 (ambos inclusive), o la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="28a50-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28a50-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28a50-116">Remarks</span></span>

<span data-ttu-id="28a50-117">La cadena resultante tiene un carácter Unicode (dos caracteres) de longitud.</span><span class="sxs-lookup"><span data-stu-id="28a50-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="28a50-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28a50-118">Example</span></span>

<span data-ttu-id="28a50-119">UNICHAR(65)</span><span class="sxs-lookup"><span data-stu-id="28a50-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="28a50-120">Devuelve un (letra latina mayúscula A)</span><span class="sxs-lookup"><span data-stu-id="28a50-120">Returns A (Latin Capital Letter A)</span></span> 
  

