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

RePLACE (* * *texto_original* * *, * * *núm_inicial* * *, * * *Núm_de_caracteres* * *, * * *texto_nuevo* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _texto_original_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto en el que desea reemplazar algunos caracteres.  <br/> |
| _Núm_inicial_ <br/> |Obligatorio  <br/> |**Number** <br/> |Posición del carácter en _texto_original_ que se desea reemplazar por _texto_nuevo_. El primer carácter de la cadena ocupa la posición 1.  <br/> |
| _Núm_de_caracteres_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número de caracteres en _texto_original_ que desea reemplazar.  <br/> |
| _argumento_ <br/> |Obligatorio  <br/> |**String** <br/> |Texto que va a reemplazar los caracteres de _texto_original_.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Comentarios

Utilice esta función cuando desee reemplazar texto que aparezca en una ubicación concreta de una cadena de texto. Si desea reemplazar un texto específico dentro de una cadena de texto, recurra a la función SUBSTITUTE.
  
## <a name="example"></a>Ejemplo

REPLACE ("01/03/2002",9,2,"03") 
  
Devuelve 01/03/2003. 
  

