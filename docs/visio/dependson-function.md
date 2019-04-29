---
title: DEPENDSON (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Crea una dependencia de referencia de celda.
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423471"
---
# <a name="dependson-function"></a>Función DEPENDSON

Crea una dependencia de referencia de celda.
  
## <a name="syntax"></a>Sintaxis

dependson (* * *cellref* * * [, * * *cellref2* * *,...]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _referenciaDeCelda_ <br/> |Obligatorio  <br/> |**String** <br/> |La primera referencia de celda.  <br/> |
| _cellref2_ <br/> |Opcional  <br/> |**String** <br/> |La segunda referencia de celda.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta función siempre devuelve el valor FALSE. No tiene ningún efecto cuando se utiliza en una celda Action o en una fila Event. 
  
## <a name="example"></a>Ejemplo

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
Abre el bloque de texto de una forma siempre que cambien las celdas PinX o PinY de la forma. 
  

