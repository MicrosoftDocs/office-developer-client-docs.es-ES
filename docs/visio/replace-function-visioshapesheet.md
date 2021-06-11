---
title: Función REPLACE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Reemplaza parte de una cadena de texto por otra cadena, de acuerdo con el número de caracteres especificado.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414357"
---
# <a name="replace-function-visioshapesheet"></a>Función REPLACE (VisioShapeSheet)

Reemplaza parte de una cadena de texto por otra cadena, de acuerdo con el número de caracteres especificado.
  
## <a name="syntax"></a>Sintaxis

REPLACE (** *old_text* **, ** *start_num* **, ** *num_chars* **, ** *new_text* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _old_text_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto en el que desea reemplazar algunos caracteres.  <br/> |
| _start_num_ <br/> |Obligatorio  <br/> |**Number** <br/> |La posición del carácter en  _old_text_ que desea reemplazar por  _new_text_. El primer carácter de la cadena ocupa la posición 1.  <br/> |
| _num_chars_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número de caracteres  _de old_text_ que desea reemplazar  <br/> |
| _new_text_ <br/> |Obligatorio  <br/> |**String** <br/> |Texto que reemplazará los caracteres de  _old_text_.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Comentarios

Utilice esta función cuando desee reemplazar texto que aparezca en una ubicación concreta de una cadena de texto. Si desea reemplazar un texto específico dentro de una cadena de texto, recurra a la función SUBSTITUTE.
  
## <a name="example"></a>Ejemplo

REPLACE ("01/03/2002",9,2,"03") 
  
Devuelve 01/03/2003. 
  

