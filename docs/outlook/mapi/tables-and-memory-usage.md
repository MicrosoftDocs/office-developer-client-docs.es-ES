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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320408"
---
# <a name="tables-and-memory-usage"></a>Uso de memoria y tablas

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un problema importante conectado a la recuperación de datos de una tabla es el uso de la memoria. La falta de memoria disponible puede provocar un error de [IMAPITable:: QueryRows](imapitable-queryrows.md) y [HrQueryAllRows](hrqueryallrows.md) , lo que devuelve un número inferior al número de filas deseado. La decisión del método o la función que se va a usar para recuperar los datos de la tabla depende de si se puede esperar que la tabla quepa en la memoria y, si no es posible, si el error es aceptable. 
  
Como no siempre es fácil determinar la cantidad de datos que se ajustarán a la memoria al mismo tiempo, MAPI proporciona instrucciones básicas para que el proveedor de servicios o aplicaciones cliente sigan. Recuerde que siempre hay excepciones, basadas en la implementación de la tabla concreta y en la forma en que se almacenan los datos subyacentes.
  
Las siguientes instrucciones pueden usarse para evaluar el uso de memoria de la tabla:
  
- Clientes que pueden tolerar el uso de memoria del espacio de trabajo ocasional en el intervalo de megabytes y suponer que no tendrán problemas para leer una tabla completa en la memoria. 
    
- Las restricciones afectan al uso de memoria de una tabla. Una tabla rigurosamente restringida con un amplio número de filas, como una tabla de contenido, puede esperarse que quepa en la memoria, mientras que una tabla grande sin restricciones no suele. 
    
- Normalmente, varias de las tablas que son propiedad de MAPI, como el estado, el perfil, el servicio de mensajes, el proveedor y las tablas de almacén de mensajes, se ajustan a la memoria. Por lo general, son tablas pequeñas. Sin embargo, hay excepciones. Por ejemplo, un proveedor de perfiles basado en servidor puede generar una tabla de perfiles más grande que no se podrá ajustar.
    
Para recuperar todas las filas de una tabla que se ajusten a la memoria sin problemas, llame a [HrQueryAllRows](hrqueryallrows.md), estableciendo el número máximo de filas en cero.
  
Para recuperar todas las filas de una tabla que puedan caber o no en la memoria, se genera un error y se llama a **HrQueryAllRows** especificando un número máximo de filas. El número máximo de filas debe establecerse en un número mayor que el número mínimo de filas necesarias. Si un cliente debe acceder a al menos 50 filas de una tabla de la fila 300, el número máximo de filas debe establecerse como mínimo en 51. 
  
Para recuperar todas las filas de una tabla que no se espera que quepan en la memoria, llame al método [IMAPITable:: QueryRows](imapitable-queryrows.md) en un bucle con un recuento de filas relativamente pequeño, como se ilustra en el siguiente ejemplo de código: 
  
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

Cuando se complete este bucle y se hayan procesado todas las filas de la tabla, __ y Crows sea cero, la posición del cursor estará normalmente en la parte inferior de la tabla. 
  
## <a name="see-also"></a>Vea también

- [Tablas MAPI](mapi-tables.md)

