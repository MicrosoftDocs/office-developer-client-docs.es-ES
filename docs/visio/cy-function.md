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
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433559"
---
# <a name="cy-function"></a>Función CY

Devuelve un valor de moneda.
  
## <a name="syntax"></a>Sintaxis

CY (* * *valor* * *, * * *idmoneda* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Opcional  <br/> |**Número o cadena** <br/> |Un número o una cadena que incluye el formato específico de moneda. Si no se especifica, el valor de moneda tiene el formato de acuerdo con el estilo moneda de la configuración regional y de idioma del sistema.  <br/> |
| _Idmoneda_ <br/> |Opcional  <br/> |**Number** <br/> |Un identificador de moneda numérico o una cadena con comillas de tres caracteres para la abreviatura ISO 4217.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para especificar una moneda distinta, debe incluir una _idmoneda_válida. Para ver una lista, vea [Constantes de moneda](about-currency-constants.md).
  
Si el _valor_ es incompatible con el tipo de moneda designado o si se ha especificado un argumento no válido, como "no es un número", #VALUE! se devuelve un error. Si el _valor_ es mayor que 922.337.203.685.477,5807 o menor que-922.337.203.685.477,5808, #VALUE! se devuelve un error. 
  
Para obtener una mayor precisión con valores de moneda muy grandes que incluyan fracciones de una unidad, como 3,6 billones, use argumentos de cadena para el _valor_.
  
Si se especifica un _idmoneda_ no válido, se devuelve un error. 
  
## <a name="example-1"></a>Ejemplo 1

Si la configuración regional y de idioma del usuario especifica dólares estadounidenses:
  
CY (999998.993)
  
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
  

