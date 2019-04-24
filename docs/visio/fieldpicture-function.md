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
description: Devuelve una cadena de formato de imagen que coincide con el código de formato interno del campo de texto de Microsoft Visio.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322550"
---
# <a name="fieldpicture-function"></a>Función FIELDPICTURE

Devuelve una cadena de formato de imagen que coincide con el código de formato interno del campo de texto de Microsoft Visio.
  
## <a name="syntax"></a>Sintaxis

FIELDPICTURE (* * *código* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Obligatorio  <br/> |**Number** <br/> | Un código de formato de campo de texto.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

Las cadenas de formato de imagen se utilizan en la función FORMAT para definir la forma de realizar la ampliación de valores para convertirlos en fechas, horas, números y etiquetas de unidades.
  
## <a name="example"></a>Ejemplo

FIELDPICTURE (0) 
  
Devuelve la cadena de formato de imagen "esc(0)", que especifica un número con un decimal y la descripción de las unidades en letras minúsculas cuando se usa en la función FORMAT. 
  

