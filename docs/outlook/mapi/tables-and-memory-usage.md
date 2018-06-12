---
title: Las tablas y el uso de memoria
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 390cec0cc59f189f83af2c5339512d82e125771e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820849"
---
# <a name="tables-and-memory-usage"></a>Las tablas y el uso de memoria

**Se aplica a**: Outlook 
  
Un problema importante conectado con la recuperación de datos de una tabla es el uso de memoria. Falta de memoria disponible puede provocar [IMAPITable:: QueryRows](imapitable-queryrows.md) y [HrQueryAllRows](hrqueryallrows.md) se lleve a cabo, devolución de menor que el número de filas que desee. Decidir qué método o función que se usará para recuperar los datos de la tabla depende de si la tabla puede esperarse que caben en la memoria y, si no se puede, si el error es aceptable. 
  
Dado que no siempre es fácil determinar la cantidad de datos que quepan en la memoria a la vez, MAPI proporciona algunas directrices básicas para una aplicación cliente o el proveedor de servicios que se deben seguir. Recuerde que siempre hay excepciones, en función de la implementación de una tabla determinada y cómo se almacenan los datos subyacentes.
  
Las siguientes instrucciones se pueden usar para evaluar el uso de memoria de tabla:
  
- Los clientes que pueden tolerar la ocasionales el uso de memoria conjunto de trabajo en el intervalo de megabyte y pueden asumir no tendrán ningún problema leer toda la tabla en la memoria. 
    
- Restricciones tienen un efecto sobre el uso de una tabla de memoria. Una tabla rigurosamente restringida con un amplio número de filas, como una tabla de contenido, puede esperarse que caben en la memoria, mientras que normalmente no una tabla de gran tamaño sin restricciones. 
    
- Varias de las tablas que pertenecen a MAPI, como el estado, perfiles, servicio de mensajes, proveedor y tablas de almacén de mensajes, normalmente quepan en la memoria. Estos son tablas pequeñas en general. Sin embargo, hay excepciones. Por ejemplo, un proveedor de perfil basado en servidor podría generar una tabla de perfil de mayor tamaño que no pueda ajustar.
    
Para recuperar todas las filas de una tabla que quepan en la memoria sin problemas, llame a [HrQueryAllRows](hrqueryallrows.md), si se establece el número máximo de filas en cero.
  
Para recuperar todas las filas de una tabla que podría o no es posible que caben en la memoria, genere un error, llame a **HrQueryAllRows** especificando un número máximo de filas. El número máximo de filas debe establecerse en un número mayor que el número mínimo de filas que se necesitan. Si un cliente debe tener acceso al menos 50 filas de una tabla de 300 filas, el número máximo de filas debe establecerse en al menos 51. 
  
Para recuperar todas las filas de una tabla que no se espera que caben en la memoria, llamada [IMAPITable:: QueryRows](imapitable-queryrows.md) en un bucle con un recuento de filas relativamente pequeño, como se muestra en el ejemplo de código siguiente: 
  
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

Cuando se complete este bucle y se hayan procesado todas las filas de la tabla y _cRows_ es cero, normalmente será la posición del cursor en la parte inferior de la tabla. 
  
## <a name="see-also"></a>Ver también

- [Tablas MAPI](mapi-tables.md)

