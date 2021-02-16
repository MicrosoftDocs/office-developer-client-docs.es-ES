---
title: Uso de memoria y tablas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: afd69f5a3fff69f670d6be78ba4957307cdb6995
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436863"
---
# <a name="tables-and-memory-usage"></a>Uso de memoria y tablas

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un problema importante relacionado con la recuperación de datos de una tabla es el uso de memoria. La falta de memoria disponible puede provocar un error [en IMAPITable::QueryRows](imapitable-queryrows.md) y [HrQueryAllRows,](hrqueryallrows.md) lo que devuelve un número menor que el número de filas deseado. Decidir qué método o función usar para recuperar datos de tabla depende de si se puede esperar que la tabla se ajuste a la memoria y, si no es posible, si el error es aceptable. 
  
Dado que no siempre es fácil determinar la cantidad de datos que caben en la memoria a la vez, MAPI proporciona algunas directrices básicas para que siga una aplicación cliente o un proveedor de servicios. Recuerde que siempre hay excepciones, en función de la implementación de tabla concreta y de cómo se almacenan los datos subyacentes.
  
Se pueden usar las siguientes instrucciones para evaluar el uso de memoria de tabla:
  
- Clientes que pueden tolerar el uso de memoria de conjunto de trabajo ocasional en el intervalo de megabytes y pueden suponer que no tendrán problemas al leer una tabla completa en la memoria. 
    
- Las restricciones afectan al uso de memoria de una tabla. Se puede esperar que una tabla con restricciones graves con un gran número de filas, como una tabla de contenido, se ajuste a la memoria, mientras que una tabla grande sin restricciones normalmente no puede. 
    
- Varias de las tablas que pertenecen a MAPI, como las tablas de estado, perfil, servicio de mensajes, proveedor y almacén de mensajes, normalmente caben en la memoria. Por lo general, se trata de tablas pequeñas. Sin embargo, hay excepciones. Por ejemplo, un proveedor de perfiles basado en servidor podría generar una tabla de perfiles más grande que no se pueda ajustar.
    
Para recuperar todas las filas de una tabla que caben en la memoria sin problemas, llame a [HrQueryAllRows](hrqueryallrows.md), estableciendo el número máximo de filas en cero.
  
Para recuperar todas las filas de una tabla que podrían o no caben en la memoria, lo que genera un error, llame a **HrQueryAllRows** especificando un número máximo de filas. El número máximo de filas debe establecerse en un número mayor que el número mínimo de filas que se necesitan. Si un cliente debe tener acceso al menos a 50 filas de una tabla de 300 filas, el número máximo de filas debe establecerse en al menos 51. 
  
Para recuperar todas las filas de una tabla que no se espera que quepa en la memoria, llame a [IMAPITable::QueryRows](imapitable-queryrows.md) en un bucle con un recuento de filas relativamente pequeño, como se muestra en el siguiente ejemplo de código: 
  
```cpp
HRESULT     hr;
LPSRowSet   pRows = NULL;
LONG        irow;
LONG            cAsk = 50;                  // adjust this value
while ((hr = pTable->QueryRows(cAsk, 0, &pRows)) == hrSuccess
        && pRows->cRows != 0)
{
    for (irow = 0; irow < prows->cRows; ++irow)
    {
        // process the row...
    }
    FreeProws(pRows);
    pRows = NULL;
}
if (hr)
{
    // handle the error...
}
 
```

Cuando este bucle se completa y se han procesado todas las filas de la tabla y  _cRows_ es cero, la posición del cursor normalmente estará en la parte inferior de la tabla. 
  
## <a name="see-also"></a>Consulte también

- [Tablas MAPI](mapi-tables.md)

