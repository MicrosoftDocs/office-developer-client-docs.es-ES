---
title: FORMATEX (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Devuelve el resultado de expresión evaluado en unidadesDeOrigen como una cadena con formato de acuerdo con el formato expresado en unidadesDeDestino.
ms.openlocfilehash: 08d123967272e0ab4e25990bcfab55cc80cef55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822200"
---
# <a name="formatex-function"></a>FORMATEX (función)

Devuelve el resultado de expresión evaluado en unidadesDeOrigen como una cadena con formato de acuerdo con el formato expresado en unidadesDeDestino.
  
## <a name="syntax"></a>Sintaxis

FORMATEX (** *expresión* **, "** *formato* **", [** *unidadesDeOrigen* **], [** *unidadesDeDestino* **], [** *langID* **] [, ** *IDcalendario* **]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor.  <br/> |
| _format_ <br/> |Obligatorio  <br/> |**String** <br/> |La imagen de formato utilizada para dar formato a la cadena. Para obtener más información acerca de las imágenes de formato, vea [Acerca de las imágenes de formato](about-format-pictures.md).  <br/> |
| _unidadesDeOrigen_ <br/> |Opcional  <br/> |**String** <br/> | Unidades usadas para evaluar expresión (PDA, cm etc.).  <br/> |
| _unidadesDeDestino_ <br/> |Opcional  <br/> |**String** <br/> |Unidades que se usará para el resultado de expresión (PDA, cm etc.).  <br/> |
| _langID_ <br/> |Opcional  <br/> |**Número** <br/> |El idioma utilizado para dar formato a las imágenes de fecha y hora de Microsoft Office System.  <br/> |
| _IDcalendario_ <br/> |Opcional  <br/> |**Número** <br/> |El calendario usado para dar formato a las imágenes de fecha y hora de Microsoft Office System.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Notas

El tipo de la expresión y el tipo especificado en el formato de imagen controlan el comportamiento de la cadena devuelta. El formato debe ser adecuado para el tipo de expresión.
  
El argumento unidadesDeOrigen se usa para escalar los resultados de expresiones sin tipo, por ejemplo 3 + 4. Si el resultado de expresión tiene un tipo explícito, como 3 ft + 8 ft, a continuación, unidadesDeOrigen se omite.
  
El argumento unidadesDeDestino se utiliza para especificar las unidades utilizadas para el resultado con formato. Si no se especifica las unidadesDeDestino, se utilizan las unidades para el resultado de la expresión.
  
Devuelve un error si el resultado de la expresión y el tipo esperado en formato son de un tipo diferente, si hay errores de sintaxis en formato o si no reconoce las unidades que se pasa como unidadesDeOrigen o unidadesDeDestino.
  
## <a name="example"></a>Ejemplo

FORMATEX(5,5; "0,00 u", "cm", "ft") 
  
Devuelve 0,18 pies. 
  

