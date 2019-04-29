---
title: Función YEAR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Devuelve un entero que representa el año gregoriano en fechaHora o expresión, con formato de acuerdo con el estilo de fecha corta establecido en la configuración regional y de idioma actual del sistema.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420713"
---
# <a name="year-function-visioshapesheet"></a>Función YEAR (VisioShapeSheet)

Devuelve un entero que representa el año gregoriano en _fechaHora_ o _expresión_, con formato de acuerdo con el estilo de fecha corta establecido en la configuración regional y de idioma actual del sistema.
  
## <a name="syntax"></a>Sintaxis

YEAR ("* * *DateTime* * *" | * * *expresión* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**Diferencias** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numérico** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

Se descarta el componente de hora de _fecha_ y hora o de _expresión_ . 
  
No se realiza redondeo. Si falta _fechaHora_ o no se puede interpretar como una fecha u hora válidas, Year devuelve un error. 
  
La función YEAR también acepta un único valor numérico en _expresión_ , en el que la parte entera del resultado representa el número de días transcurridos desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

AÑO ("10/27/2007 13:45:24")
  
Devuelve 2007.
  
## <a name="example-2"></a>Ejemplo 2

YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)
  
Devuelve 2007.
  
## <a name="example-3"></a>Ejemplo 3

AÑO (35580.6337)
  
Devuelve 1997.
  

