---
title: IS [NOT] NULL (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Determina si una expresión especificada es NULL.
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815337"
---
# <a name="is-not-null-access-custom-web-app"></a>IS [NOT] NULL (aplicación web personalizada de Access)

Determina si una expresión especificada es NULL.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/es-ES/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 *expression* **IS** [  *NOT*  ] **NULL**
  
El predicado **IS [NOT] NULL** contiene los siguientes argumentos. 
  
|||
|:-----|:-----|
| *expression*  <br/> |Cualquier expresión válida.  <br/> |
| *NOT*  <br/> |Especifica que se niega el resultado Boolean. El predicado invierte los valores devueltos, devolviendo TRUE si el valor no es NULL y FALSE si el valor es NULL.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el valor de  *expresión*  es NULL, IS NULL devuelve TRUE; de lo contrario, devuelve FALSE. 
  
Si el valor de la expresión es NULL, IS NOT NULL devuelve FALSE; de lo contrario, devuelve TRUE.
  

