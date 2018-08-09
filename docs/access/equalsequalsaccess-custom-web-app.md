---
title: Es igual a (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compara la igualdad de dos expresiones.
ms.openlocfilehash: efdd06a1735190d63c13c4df8230e1d29d71c1dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815347"
---
# <a name="equals-access-custom-web-app"></a>Es igual a (aplicación web personalizado de Access)

Compara la igualdad de dos expresiones.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

`= (Equals)`

*expresión*  =  *expresión* 
  
*expresión*  Es cualquier expresión válida. Si las expresiones no son del mismo tipo de datos, el tipo de datos para una expresión debe ser implícitamente convertible al tipo de datos de la otra. La conversión depende de las reglas de precedencia de tipo de datos. 
  
## <a name="return-type"></a>Tipo de valor devuelto

**Boolean**
  
## <a name="remarks"></a>Comentarios

Cuando se comparan dos expresiones NULL, el resultado es TRUE.
  
Comparación de NULL en un valor no nulo siempre da como resultado FALSE.
  

