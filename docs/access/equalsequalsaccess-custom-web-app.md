---
title: Equals(Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compara la igualdad de dos expresiones.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408932"
---
# <a name="equals-access-custom-web-app"></a>Igual a (aplicación web personalizada de Access)

Compara la igualdad de dos expresiones.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

`= (Equals)`

*expresión*   =   *expresión* 
  
*expresión*  Es cualquier expresión válida. Si las expresiones no son del mismo tipo de datos, el tipo de datos de una expresión debe ser implícitamente convertible para el tipo de datos de la otra. La conversión depende de las reglas de prioridad del tipo de datos. 
  
## <a name="return-type"></a>Tipo de valor devuelto

**Boolean**
  
## <a name="remarks"></a>Comentarios

Cuando se comparan dos expresiones NULL, el resultado es TRUE.
  
La comparación de NULL con un valor que no es NULL siempre da como resultado FALSE.
  

