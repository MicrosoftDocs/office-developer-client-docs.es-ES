---
title: EVALTEXT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Evalúa el texto que contiene nombreDeForma como si fuera una fórmula y devuelve el resultado.
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822081"
---
# <a name="evaltext-function"></a>EVALTEXT (función)

Evalúa el texto que _contiene nombreDeForma_ como si fuera una fórmula y devuelve el resultado. 
  
## <a name="syntax"></a>Sintaxis

EVALTEXT (** *nombreDeForma! theText* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombreDeForma! theText_ <br/> |Obligatorio  <br/> |**String** <br/> |Una celda que se desencadena cuando cambia la composición texto de la forma asociada.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Notas

 _nombreDeForma_ se puede usar para hacer referencia al texto de una forma que no sea la forma actual. 
  
Si no hay ningún texto, el resultado es cero. Si el texto no se puede evaluar, la función devuelve un error.
  
## <a name="example"></a>Ejemplo

EVALTEXT(Line.2!TheText) 
  
Evalúa el texto que contiene la forma Línea.2. Por ejemplo, si Línea.2 contiene "4 cm + 0,5 cm", devuelve el valor 4,5 cm. 
  

