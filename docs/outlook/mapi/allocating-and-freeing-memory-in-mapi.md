---
title: Asignación y liberar memoria en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 68250c5cbeaa366ed4555bb469c4e68d62302f28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419670"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Asignación y liberar memoria en MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Además de especificar cómo asignar y liberar memoria, MAPI define un modelo para saber cuándo se debe liberar la memoria pasada entre el método de interfaz pública y las llamadas de función de API. El modelo se aplica solo a la memoria asignada para parámetros que no son punteros a interfaces, como cadenas y punteros a estructuras. Los punteros de interfaz usan el mecanismo de recuento de referencias implementado a través **de IUnknown**. Al asignar y liberar memoria no relacionada con MAPI internamente dentro de una aplicación cliente o proveedor de servicios, use cualquier mecanismo que tenga sentido. 
  
El modelo define los parámetros como uno de tres tipos. Pueden ser parámetros de entrada, establecidos por el autor de la llamada con información que usará la función o método llamado, parámetros de salida, establecidos por la función o método llamado y devueltos al llamador, o parámetros de entrada y salida, una combinación de los dos tipos. Los parámetros de salida suelen ser punteros a datos o punteros a punteros a datos. Aunque la función a la que se llama es responsable de asignar los datos para los parámetros de salida, el autor de la llamada asigna la memoria para el puntero. 
  
Las reglas para asignar y liberar memoria para estos tipos de parámetros se explican en la tabla siguiente.
  
|**Tipo**|**Asignación de memoria**|**Versión de memoria**|
|:-----|:-----|:-----|
|Input  <br/> |El autor de la llamada es responsable y puede usar cualquier mecanismo.  <br/> |El autor de la llamada es responsable y puede usar cualquier mecanismo.  <br/> |
|Salida  <br/> |La función llamada es responsable y debe usar **MAPIAllocateBuffer**. Para obtener más información, [vea MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |El autor de la llamada es responsable y debe **usar MAPIFreeBuffer**. Para obtener más información, vea [MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|Entrada y salida  <br/> |El autor de la llamada es responsable de la asignación inicial y la función llamada puede volver a asignarse si es necesario mediante **MAPIAllocateBuffer**.  <br/> |La función llamada es responsable de la liberación inicial si es necesario reasignar. El autor de la llamada debe liberar el valor devuelto final.  <br/> |
   
Durante las condiciones de error, los implementadores de los métodos de interfaz deben prestar atención a los parámetros de salida y salida de entrada porque, por lo general, el llamador no tiene forma de limpiarlos. Si se devuelve un error, cada parámetro de salida o de entrada-salida debe dejarse en el valor inicializado por el autor de la llamada o establecerse en un valor que se pueda limpiar sin ninguna acción por parte del autor de la llamada. Por ejemplo, un parámetro de puntero de salida debe dejarse tal como estaba en la entrada o puede establecerse  `void ** ppv` en NULL (  `*ppv = NULL` ).
  

