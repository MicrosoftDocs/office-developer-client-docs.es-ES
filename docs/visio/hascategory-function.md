---
title: HASCATEGORY (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Devuelve TRUE si la cadena especificada se encuentra en la lista de categorías de la forma.
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360168"
---
# <a name="hascategory-function"></a>Función HASCATEGORY

Devuelve TRUE si la cadena especificada se encuentra en la lista de categorías de la forma.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

HASCATEGORY (* * *categoría* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _Categoría_ <br/> |Obligatorio  <br/> |**String** <br/> |Categoría que se va a buscar.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Boolean**
  
## <a name="remarks"></a>Observaciones

 Las *categorías* son cadenas definidas por el usuario que puede usar para clasificar formas. Las categorías se pueden definir en la celda User.msvShapeCategories, en la ShapeSheet de una forma. Puede definir varias categorías relativas a una forma si las separa con punto y coma. 
  

