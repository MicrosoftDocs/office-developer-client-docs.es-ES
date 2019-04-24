---
title: Asignar y liberar memoria en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 68250c5cbeaa366ed4555bb469c4e68d62302f28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281588"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Asignar y liberar memoria en MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Además de especificar cómo asignar y liberar memoria, MAPI define un modelo para saber cuándo se debe liberar la memoria que entre el método de interfaz pública y las llamadas de función de la API. El modelo se aplica únicamente a la memoria asignada para los parámetros que no son punteros a las interfaces, como cadenas y punteros a estructuras. Los punteros de interfaz usan el mecanismo de recuento de referencias implementado a través de **IUnknown**. Al asignar y liberar internamente memoria no relacionada con MAPI dentro de una aplicación cliente o un proveedor de servicios, use cualquier mecanismo que tenga sentido. 
  
El modelo define los parámetros como uno de estos tres tipos. Pueden ser parámetros de entrada, establecidos por el autor de la llamada con información que va a usar la función o el método al que se ha llamado, los parámetros de salida, establecidos por la función o el método con el que se ha devuelto la llamada, o los parámetros de entrada-salida, una combinación de ambos tipos. Los parámetros de salida son punteros frecuentes a datos o punteros a punteros a datos. Aunque la función llamada es responsable de asignar los datos para los parámetros de salida, el autor de la llamada asigna la memoria del puntero. 
  
En la tabla siguiente se explican las reglas para asignar y liberar memoria para estos tipos de parámetros.
  
|**Type**|**Asignación de memoria**|**Liberar memoria**|
|:-----|:-----|:-----|
|Input  <br/> |El autor de la llamada es responsable y puede usar cualquier mecanismo.  <br/> |El autor de la llamada es responsable y puede usar cualquier mecanismo.  <br/> |
|Output  <br/> |La función llamada es responsable y debe usar **MAPIAllocateBuffer**. Para obtener más información, vea [MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |El autor de la llamada es responsable y debe usar **MAPIFreeBuffer**. Para obtener más información, vea [MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|Input-Output  <br/> |El autor de la llamada es responsable de la asignación inicial y la función a la que se llama puede reasignar si es necesario usando **MAPIAllocateBuffer**.  <br/> |La función llamada es responsable de la liberación inicial si es necesaria la reasignación. El autor de la llamada debe liberar el valor devuelto final.  <br/> |
   
En las condiciones de error, los implementadores de los métodos de interfaz necesitan prestar atención a los parámetros de salida y de salida de entrada, ya que el autor de la llamada no suele tener forma de limpiarlos. Si se devuelve un error, cada parámetro de salida o entrada-salida debe dejarse en el valor inicializado por el autor de la llamada o establecerse en un valor que se puede limpiar sin realizar ninguna acción por parte del autor de la llamada. Por ejemplo, un parámetro de salida de puntero `void ** ppv` -parámetro de debe dejarse como estaba en la entrada o puede establecerse `*ppv = NULL`en null ().
  

