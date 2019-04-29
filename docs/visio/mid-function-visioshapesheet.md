---
title: Función MID (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Devuelve un número específico de caracteres de una cadena de texto, comenzando en la posición especificada, en función del número de caracteres que se especifique.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410269"
---
# <a name="mid-function-visioshapesheet"></a>Función MID (VisioShapeSheet)

Devuelve un número específico de caracteres de una cadena de texto, comenzando en la posición especificada, en función del número de caracteres que se especifique.
  
## <a name="syntax"></a>Sintaxis

MID (* * *texto* * *, * * *núm_inicial* * *, * * *Núm_de_caracteres* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> |La cadena de texto que contiene los caracteres que se desean extraer.  <br/> |
| _Núm_inicial_ <br/> |Obligatorio  <br/> |**Number** <br/> |La posición del primer carácter que se desea extraer. El primer carácter de la cadena de texto ocupa la posición 1.  <br/> |
| _Núm_de_caracteres_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número de caracteres que debe devolverse.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Comentarios

Si *núm_inicial* es: 
  
- Mayor que la longitud de *texto* , Mid devuelve "" (texto vacío). 
    
- Menor que la longitud de *texto* , pero *núm_inicial* más *Núm_de_caracteres* supera la longitud del *texto* , Mid devuelve los caracteres hasta el final del *texto* . 
    
- Menor que 1, MID devuelve el #VALUE! valor de error. 
    
Si *Núm_de_caracteres* es negativo, Mid devuelve el #VALUE! valor de error. 
  
## <a name="example"></a>Ejemplo

MID ("SSN 999-99-9999",5,11) 
  
Devuelve 999-99-9999. 
  

