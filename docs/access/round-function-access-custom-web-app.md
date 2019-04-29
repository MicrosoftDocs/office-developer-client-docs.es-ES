---
title: Función Round (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Devuelve un valor numérico, redondeado o truncado, con la longitud o precisión especificada.
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413748"
---
# <a name="round-function-access-custom-web-app"></a><span data-ttu-id="83cc5-103">Función Round (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="83cc5-103">Round Function (Access custom web app)</span></span>

<span data-ttu-id="83cc5-104">Devuelve un valor numérico, redondeado o truncado, con la longitud o precisión especificada.</span><span class="sxs-lookup"><span data-stu-id="83cc5-104">Returns a numeric value, either rounded or truncated, to the specified length or precision.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="83cc5-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="83cc5-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="83cc5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83cc5-107">Syntax</span></span>

 <span data-ttu-id="83cc5-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span><span class="sxs-lookup"><span data-stu-id="83cc5-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span></span> 
  
<span data-ttu-id="83cc5-109">La función **Round** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="83cc5-109">The **Round** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="83cc5-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="83cc5-110">**Argument name**</span></span>|<span data-ttu-id="83cc5-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83cc5-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="83cc5-112">*Número*</span><span class="sxs-lookup"><span data-stu-id="83cc5-112">*Number*</span></span>  <br/> |<span data-ttu-id="83cc5-113">Expresión numérica.</span><span class="sxs-lookup"><span data-stu-id="83cc5-113">A numeric expression.</span></span>  <br/> |
| <span data-ttu-id="83cc5-114">*Precision*</span><span class="sxs-lookup"><span data-stu-id="83cc5-114">*Precision*</span></span>  <br/> |<span data-ttu-id="83cc5-p102">Precisión con la que se redondeará el argumento  *Number*  . El argumento  *Precision*  debe ser una expresión numérica. Cuando  *Precision*  sea un número positivo, el argumento  *Number*  se redondeará al número de posiciones decimales especificado por el valor de longitud. Cuando  *Precision*  sea un número negativo, el argumento  *Number*  se redondea en la izquierda de la coma, según especifique el valor de longitud.  </span><span class="sxs-lookup"><span data-stu-id="83cc5-p102">The precision to which  *Number*  is to be rounded.  *Precision*  must be a numeric expression. When  *Precision*  is a positive number,  *Number*  is rounded to the number of decimal positions specified by length. When  *Precision*  is a negative number,  *Number*  is rounded on the left side of the decimal point, as specified by length.  </span></span><br/> |
| <span data-ttu-id="83cc5-119">*TruncateInsteadOfRound*</span><span class="sxs-lookup"><span data-stu-id="83cc5-119">*TruncateInsteadOfRound*</span></span>  <br/> |<span data-ttu-id="83cc5-p103">Tipo de operación que se va a realizar. Cuando se omite o se establece en 0, el argumento  *Number*  se redondea. Cuando se especifica un valor distinto de 0, el argumento  *Number*  se trunca. El valor predeterminado es 0.  </span><span class="sxs-lookup"><span data-stu-id="83cc5-p103">The type of operation to perform. When omitted or set to 0,  *Number*  is rounded. When a value other than 0 is specified,  *Number*  is truncated. The default value is 0.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="83cc5-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83cc5-124">Remarks</span></span>

 <span data-ttu-id="83cc5-p104">**Round** siempre devuelve un valor. Si el valor de longitud es negativo y mayor que el número de dígitos antes de la coma decimal, **Round** devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="83cc5-p104">**Round** always returns a value. If length is negative and larger than the number of digits before the decimal point, **Round** returns 0.</span></span> 
  

