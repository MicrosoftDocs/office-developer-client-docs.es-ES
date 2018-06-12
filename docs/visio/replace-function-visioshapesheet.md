---
title: Reemplace la función (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Reemplaza parte de una cadena de texto por otra cadena, de acuerdo con el número de caracteres especificado.
ms.openlocfilehash: 4112339d772248ac033674808d97c3f9c55b6f0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822946"
---
# <a name="replace-function-visioshapesheet"></a>Reemplace la función (VisioShapeSheet)

Reemplaza parte de una cadena de texto por otra cadena, de acuerdo con el número de caracteres especificado.
  
## <a name="syntax"></a>Sintaxis

Reemplazar (** *texto_anterior* **, ** *número_inicio* **, ** *número_caracteres* **, ** *texto_nuevo* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _texto original_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto en el que desea reemplazar algunos caracteres.  <br/> |
| _número inicial_ <br/> |Obligatorio  <br/> |**Número** <br/> |La posición del carácter en _texto_anterior_ que se desea reemplazar por _texto_nuevo_. El primer carácter de la cadena es la posición 1.  <br/> |
| _número_caracteres_ <br/> |Obligatorio  <br/> |**Número** <br/> |El número de caracteres en _texto_anterior_ que se desea reemplazar  <br/> |
| _texto_nuevo_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto que reemplazará los caracteres en _texto_anterior_.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Observaciones

Utilice esta función cuando desee reemplazar texto que aparezca en una ubicación concreta de una cadena de texto. Si desea reemplazar un texto específico dentro de una cadena de texto, recurra a la función SUBSTITUTE.
  
## <a name="example"></a>Ejemplo

REPLACE ("01/03/2002",9,2,"03") 
  
Devuelve 01/03/2003. 
  

