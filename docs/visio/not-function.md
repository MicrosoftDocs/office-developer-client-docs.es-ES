---
title: NOT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Devuelve TRUE (1) si la expresión lógica es FALSE. De lo contrario, devuelve FALSE (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413335"
---
# <a name="not-function"></a><span data-ttu-id="55258-104">Función NOT</span><span class="sxs-lookup"><span data-stu-id="55258-104">NOT Function</span></span>

<span data-ttu-id="55258-105">Devuelve TRUE (1) si  _la expresión lógica_ es FALSE.</span><span class="sxs-lookup"><span data-stu-id="55258-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="55258-106">De lo contrario, devuelve FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="55258-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="55258-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55258-107">Syntax</span></span>

<span data-ttu-id="55258-108">NOT(\*\* *logicalexpression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="55258-108">NOT(\*\* *logicalexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="55258-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55258-109">Parameters</span></span>

|<span data-ttu-id="55258-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="55258-110">**Name**</span></span>|<span data-ttu-id="55258-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="55258-111">**Required/Optional**</span></span>|<span data-ttu-id="55258-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="55258-112">**Data Type**</span></span>|<span data-ttu-id="55258-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55258-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="55258-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="55258-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="55258-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="55258-115">Required</span></span>  <br/> |<span data-ttu-id="55258-116">**String**</span><span class="sxs-lookup"><span data-stu-id="55258-116">**String**</span></span> <br/> |<span data-ttu-id="55258-117">La expresión lógica por evaluar.</span><span class="sxs-lookup"><span data-stu-id="55258-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="55258-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55258-118">Return value</span></span>

<span data-ttu-id="55258-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="55258-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="55258-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55258-120">Example</span></span>

<span data-ttu-id="55258-121">NOT(Height \> 0,75 in)</span><span class="sxs-lookup"><span data-stu-id="55258-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="55258-122">Devuelve 1 si Height es menor o igual que 0,75 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="55258-122">Returns 1 if Height is less than or equal to 0.75 inches.</span></span> <span data-ttu-id="55258-123">Devuelve 0 si Height es mayor que 0,75 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="55258-123">Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

