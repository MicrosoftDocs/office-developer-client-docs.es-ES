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
description: Evalúa el texto en nombredeforma como si fuera una fórmula y devuelve el resultado.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329053"
---
# <a name="evaltext-function"></a>Función EVALTEXT

Evalúa el texto en _nombredeforma_ como si fuera una fórmula y devuelve el resultado. 
  
## <a name="syntax"></a>Sintaxis

EVALTEXT (* * *nombredeforma! el texto* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombredeforma! TheText_ <br/> |Obligatorio  <br/> |**String** <br/> |Una celda que se desencadena cuando cambia la composición texto de la forma asociada.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

 _nombreDeForma_ se puede usar para hacer referencia al texto de una forma que no es la actual. 
  
Si no hay ningún texto, el resultado es cero. Si el texto no se puede evaluar, la función devuelve un error.
  
## <a name="example"></a>Ejemplo

EVALTEXT (line. 2! TheText) 
  
Evalúa el texto que contiene la forma Línea.2. Por ejemplo, si Línea.2 contiene "4 cm + 0,5 cm", devuelve el valor 4,5 cm. 
  

