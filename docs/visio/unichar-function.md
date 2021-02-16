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
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417584"
---
# <a name="unichar-function"></a><span data-ttu-id="2002c-103">Función UNICHAR</span><span class="sxs-lookup"><span data-stu-id="2002c-103">UNICHAR Function</span></span>

<span data-ttu-id="2002c-104">Devuelve el carácter Unicode de un número.</span><span class="sxs-lookup"><span data-stu-id="2002c-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2002c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2002c-105">Syntax</span></span>

<span data-ttu-id="2002c-106">UNICHAR (\*\* *number* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2002c-106">UNICHAR (\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2002c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2002c-107">Parameters</span></span>

|<span data-ttu-id="2002c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2002c-108">**Name**</span></span>|<span data-ttu-id="2002c-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="2002c-109">**Required/Optional**</span></span>|<span data-ttu-id="2002c-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2002c-110">**Data Type**</span></span>|<span data-ttu-id="2002c-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2002c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2002c-112">_number_</span><span class="sxs-lookup"><span data-stu-id="2002c-112">_number_</span></span> <br/> |<span data-ttu-id="2002c-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2002c-113">Required</span></span>  <br/> |<span data-ttu-id="2002c-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="2002c-114">**Integer**</span></span> <br/> |<span data-ttu-id="2002c-115">Debe ser un entero comprendido entre 1 y 65.535 (ambos inclusive), o la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="2002c-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2002c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2002c-116">Remarks</span></span>

<span data-ttu-id="2002c-117">La cadena resultante tiene un carácter Unicode (dos caracteres) de longitud.</span><span class="sxs-lookup"><span data-stu-id="2002c-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2002c-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2002c-118">Example</span></span>

<span data-ttu-id="2002c-119">UNICHAR(65)</span><span class="sxs-lookup"><span data-stu-id="2002c-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="2002c-120">Devuelve A (letra A mayúscula latina)</span><span class="sxs-lookup"><span data-stu-id="2002c-120">Returns A (Latin Capital Letter A)</span></span> 
  

