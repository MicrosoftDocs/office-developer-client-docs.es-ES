---
title: CY (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Devuelve un valor de moneda.
ms.openlocfilehash: ea7696e7628939466730b9c054a706a7a9fa264e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821890"
---
# <a name="cy-function"></a>Función CY

Devuelve un valor de moneda.
  
## <a name="syntax"></a>Sintaxis

CY (** *valor* **, ** *IdMoneda* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Opcional  <br/> |**Número o cadena** <br/> |Un número o una cadena que incluye el formato específico de la moneda. Si no se especifica, el valor de moneda tiene el formato según el estilo de moneda en la configuración del sistema regional y de idioma.  <br/> |
| _IdMoneda_ <br/> |Opcional  <br/> |**Número** <br/> |Un ID de moneda numérica o una cadena entrecomillada de tres caracteres de la abreviatura de ISO 4217.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para especificar una moneda diferente, debe incluir un _IdMoneda_de válido. Para obtener una lista, vea [acerca de las constantes de moneda](about-currency-constants.md).
  
Si el _valor_ no es compatible con el tipo de moneda designado, o si es un argumento no válido, como "no es un número" especificado, #VALUE! se devuelve el error. Si el _valor_ es mayor que 922.337.203.685.477,5807 o menor que -922.337.203.685.477,5808, #VALUE! se devuelve el error. 
  
Para mejorar la precisión con valores de moneda muy grandes que incluyan fracciones de unidad, como 3,6 billones, utilice argumentos de _valor de_cadena.
  
Especifica un _IdMoneda_ de no válido, devuelve un error. 
  
## <a name="example-1"></a>Ejemplo 1

Si la configuración regional y de idioma del usuario especifica dólares estadounidenses:
  
CY(999998.993)
  
Devuelve $999.998,99
  
## <a name="example-2"></a>Ejemplo 2

CY(12345678,993; "USD")
  
Devuelve $12.345.678,99
  
## <a name="example-3"></a>Ejemplo 3

CY(12345678,993; "DEM")
  
Devuelve 12.345.678,99 DEM
  
## <a name="example-4"></a>Ejemplo 4

CY(12345678,7832; "XXX")
  
Devuelve 12.345.678,78
  

