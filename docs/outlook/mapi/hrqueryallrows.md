---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422897"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera todas las filas de una tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a>Parameters

 _tabla ptable_
  
> [in] Puntero a la tabla MAPI desde la que se recuperan las filas. 
    
 _ptaga_
  
> [in] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedades que indican columnas de tabla. Estas etiquetas se usan para seleccionar las columnas específicas que se van a recuperar. Si el _parámetro ptaga_ es NULL, **HrQueryAllRows** recupera todo el conjunto de columnas de la vista de tabla actual pasada en el _parámetro ptable._ 
    
 _pres_
  
> [in] Puntero a una [estructura SRestriction](srestriction.md) que contiene restricciones de recuperación. Si el  _parámetro pres_ es NULL, **HrQueryAllRows** no realiza ninguna restricción. 
    
 _psos_
  
> [in] Puntero a una [estructura SSortOrderSet](ssortorderset.md) que identifica el criterio de ordenación de las columnas que se recuperarán. Si el  _parámetro psos_ es NULL, se usa el criterio de ordenación predeterminado para la tabla. 
    
 _crowsMax_
  
> [in] Número máximo de filas que se recuperarán. Si el valor del parámetro  _crowsMax_ es cero, no se establece ningún límite en el número de filas recuperadas. 
    
 _pprows_
  
> [salida] Puntero a un puntero a la estructura [SRowSet](srowset.md) devuelta que contiene una matriz de punteros a las filas de tabla recuperadas. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada recuperó las filas esperadas de una tabla. 
    
MAPI_E_TABLE_TOO_BIG 
  
> El número de filas de la tabla es mayor que el número pasado para el _parámetro crowsMax._ 
    
## <a name="remarks"></a>Comentarios

Una aplicación cliente o proveedor de servicios no tiene control sobre el número de filas que **HrQueryAllRows** intenta recuperar, aparte de imponer una restricción señalada por el _parámetro pres._ El  _parámetro crowsMax_ no limita la recuperación a un número determinado de filas de tabla, sino que define una cantidad máxima de memoria disponible para contener todas las filas recuperadas. La única protección contra el desbordamiento masivo de memoria es la característica stopgap proporcionada al  _establecer crowsMax_. El error MAPI_E_TABLE_TOO_BIG significa que la tabla contiene demasiadas filas que se deben tener todas a la vez en la memoria. 
  
Las tablas que suelen ser pequeñas, como una tabla de almacén de mensajes o una tabla de proveedor, normalmente se pueden recuperar con seguridad con **HrQueryAllRows**. Las tablas en riesgo de ser muy grandes, como una tabla de contenido o incluso una tabla de destinatarios, deben recorrerse en subsecciones mediante el método [IMAPITable::QueryRows.](imapitable-queryrows.md) 
  
Si alguna de las propiedades de tabla no está definida cuando se llama a **HrQueryAllRows,** se devuelven con el tipo de propiedad PT_NULL y el identificador de PROP_ID_NULL 
  

