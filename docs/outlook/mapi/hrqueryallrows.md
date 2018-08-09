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
ms.openlocfilehash: 5c62e5919c6e605aa4b60f48072996ed1fd4c355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817071"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**Hace referencia a**: Outlook 
  
Recupera todas las filas de una tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
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

## <a name="parameters"></a>Parámetros

 _pTable_
  
> [entrada] Puntero a la tabla MAPI desde la que se recuperan las filas. 
    
 _ptaga_
  
> [entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de propiedad de etiquetas que indica las columnas de tabla. Estas etiquetas se usan para seleccionar las columnas específicas que se va a recuperar. Si el parámetro _ptaga_ es NULL, **HrQueryAllRows** recupera el conjunto de toda la columna de la vista de tabla actual pasada en el parámetro _ptable_ . 
    
 _Pres_
  
> [entrada] Puntero a una estructura [SRestriction](srestriction.md) que contiene las restricciones de recuperación. Si el parámetro _pres_ es NULL, **HrQueryAllRows** no realiza restricciones. 
    
 _PSO_
  
> [entrada] Puntero a una estructura [SSortOrderSet](ssortorderset.md) que identifica el criterio de ordenación de las columnas que se va a recuperar. Si el parámetro _PSO_ es NULL, se utiliza el criterio de ordenación predeterminado para la tabla. 
    
 _crowsMax_
  
> [entrada] Número máximo de filas que se va a recuperar. Si el valor del parámetro _crowsMax_ es cero, no se establece ningún límite en el número de filas recuperadas. 
    
 _ppRows_
  
> [out] Puntero a un puntero a la estructura [SRowSet](srowset.md) devuelta que contiene una matriz de punteros a las filas de tabla recuperada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada recupera las filas de una tabla esperadas. 
    
MAPI_E_TABLE_TOO_BIG 
  
> El número de filas de la tabla es mayor que el número que se pasa para el parámetro _crowsMax_ . 
    
## <a name="remarks"></a>Comentarios

Una aplicación de cliente o un proveedor de servicios no tiene control sobre el número de filas **que hrqueryallrows** intenta recuperar, además de por imponer una restricción indicada por el parámetro _pres_ . El parámetro _crowsMax_ no limitan la recuperación a un determinado número de filas de la tabla, pero en lugar de define una cantidad máxima de memoria disponible para contener las filas recuperadas todo. La única protección contra el desbordamiento de memoria masiva es la característica de provisional proporcionada estableciendo _crowsMax_. El error devuelto MAPI_E_TABLE_TOO_BIG significa que la tabla contiene demasiadas filas que se retenga todos a la vez en la memoria. 
  
Las tablas que suelen ser pequeños, por ejemplo, una tabla de almacén de mensaje o un proveedor, normalmente se pueden con seguridad recuperar con **HrQueryAllRows**. Tablas en riesgo de ser muy grande, como una tabla de contenido o incluso de una tabla de destinatarios, deben ser recorren en subsecciones utilizando el método [IMAPITable:: QueryRows](imapitable-queryrows.md) . 
  
Si las propiedades de la tabla están definidas, cuando se llama a **HrQueryAllRows** , se devuelven con el tipo de propiedad PT_NULL y el identificador de la propiedad PROP_ID_NULL 
  

