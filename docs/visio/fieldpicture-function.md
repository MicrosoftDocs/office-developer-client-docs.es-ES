---
title: FIELDPICTURE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Devuelve una cadena de formato de imagen que coincide con el código de formato de campo de texto interno de Microsoft Visio.
ms.openlocfilehash: 1528cefd65ed0c7c1dde02fa390babf26442b4d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822105"
---
# <a name="fieldpicture-function"></a>FIELDPICTURE (función)

Devuelve una cadena de formato de imagen que coincide con el código de formato de campo de texto interno de Microsoft Visio.
  
## <a name="syntax"></a>Sintaxis

FIELDPICTURE (** *código* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Obligatorio  <br/> |**Número** <br/> | Un código de formato de campo de texto.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Observaciones

Las cadenas de formato de imagen se utilizan en la función FORMAT para definir la forma de realizar la ampliación de valores para convertirlos en fechas, horas, números y etiquetas de unidades.
  
## <a name="example"></a>Ejemplo

FIELDPICTURE(0) 
  
Devuelve la cadena de formato de imagen "esc(0)", que especifica un número con un decimal y la descripción de las unidades en letras minúsculas cuando se usa en la función FORMAT. 
  

