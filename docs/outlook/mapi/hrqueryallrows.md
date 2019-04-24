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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348247"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera todas las filas de una tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
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

 _ptable_
  
> a Puntero a la tabla MAPI desde la que se recuperan las filas. 
    
 _ptaga_
  
> a Puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indica las columnas de la tabla. Estas etiquetas se usan para seleccionar las columnas específicas que se van a recuperar. Si el parámetro _ptaga_ es null, **HrQueryAllRows** recupera todo el conjunto de columnas de la vista de tabla actual pasada en el parámetro _ptable_ . 
    
 _impresa_
  
> a Puntero a una estructura [SRestriction](srestriction.md) que contiene restricciones de recuperación. Si el parámetro _Pres_ es null, **HrQueryAllRows** no realiza ninguna restricción. 
    
 _PSO_
  
> a Puntero a una estructura [SSortOrderSet](ssortorderset.md) que identifica el criterio de ordenación de las columnas que se van a recuperar. Si el parámetro _PSO_ es null, se usa el criterio de ordenación predeterminado para la tabla. 
    
 _crowsMax_
  
> a Número máximo de filas que se va a recuperar. Si el valor del parámetro _crowsMax_ es cero, no se establece ningún límite en el número de filas recuperadas. 
    
 _ppRows_
  
> contempla Puntero a un puntero a la estructura [SRowSet](srowset.md) devuelta que contiene una matriz de punteros a las filas de tabla recuperadas. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada recuperó las filas esperadas de una tabla. 
    
MAPI_E_TABLE_TOO_BIG 
  
> El número de filas de la tabla es mayor que el número pasado para el parámetro _crowsMax_ . 
    
## <a name="remarks"></a>Comentarios

Una aplicación cliente o un proveedor de servicios no tiene control sobre el número de filas que **HrQueryAllRows** intenta recuperar, a excepción de la imposición de una restricción a la que apunta el parámetro _Pres_ . El parámetro _crowsMax_ no limita la recuperación a un número determinado de filas de tabla, sino que define una cantidad máxima de memoria disponible para contener todas las filas recuperadas. La única protección contra el desbordamiento de memoria masivo es la característica provisional que proporciona la configuración de _crowsMax_. El MAPI_E_TABLE_TOO_BIG de devolución de error significa que la tabla contiene demasiadas filas que se mantendrán todas a la vez en la memoria. 
  
Normalmente, las tablas pequeñas, como una tabla de almacén de mensajes o una tabla de proveedor, se pueden recuperar con seguridad con **HrQueryAllRows**. Las tablas con riesgo de ser muy grandes, como una tabla de contenido o incluso una tabla de destinatarios, deben atravesarse en subsecciones mediante el método [IMAPITable:: QueryRows](imapitable-queryrows.md) . 
  
Si no se define ninguna propiedad de la tabla cuando se llama a **HrQueryAllRows** , se devuelven con el tipo de propiedad PT_NULL y el identificador de propiedad PROP_ID_NULL 
  

