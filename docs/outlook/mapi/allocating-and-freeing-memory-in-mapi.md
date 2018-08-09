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
ms.openlocfilehash: dc97abcb4b316b696032f2788f4e653717e1396b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816418"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Asignar y liberar memoria en MAPI

  
  
**Hace referencia a**: Outlook 
  
Además de especificar cómo asignar y liberar memoria, MAPI define un modelo para saber cuándo memoria se pasa entre el método de interfaz pública y función de la API deben liberarse a las llamadas. El modelo se aplica sólo a la memoria asignada para los parámetros que no sean punteros a las interfaces, como cadenas y punteros a estructuras. Punteros de interfaz usar el mecanismo de implementada a través de **IUnknown**de recuento de referencias. Al asignar y liberar MAPI no relacionadas con la memoria internamente dentro de una aplicación de cliente o un proveedor de servicios, use cualquier mecanismo sentido. 
  
El modelo define parámetros como uno de los tres tipos. Puede introducir parámetros, establecidos por el autor de la llamada con información que va a usar la función o método llamado, parámetros de salida, establecido por el método o la función llamada y devuelto para el autor de la llamada, o los parámetros de entrada y salida, una combinación de los dos tipos. Los parámetros de salida con frecuencia son punteros a los datos o punteros a punteros a los datos. Aunque la función llamada es responsable de asignar los datos para los parámetros de salida, el autor de la llamada asigna la memoria para el puntero. 
  
Las reglas para asignar y liberar memoria para estos tipos de los parámetros se explican en la siguiente tabla.
  
|**Tipo**|**Asignación de memoria**|**Versión de memoria**|
|:-----|:-----|:-----|
|Input  <br/> |Autor de la llamada es responsable y puede usar cualquier mecanismo.  <br/> |Autor de la llamada es responsable y puede usar cualquier mecanismo.  <br/> |
|Output  <br/> |Función llamada es responsable y debe usar **MAPIAllocateBuffer**. Para obtener más información, vea [MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |Autor de la llamada es responsable y debe usar **MAPIFreeBuffer**. Para obtener más información, vea [MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|De entrada y salida  <br/> |Autor de la llamada es responsable de la asignación inicial y la función llamada pueden reasignar si es necesario mediante **MAPIAllocateBuffer**.  <br/> |Función llamada es responsable de liberar inicial si es necesaria reasignación. Autor de la llamada debe liberar el valor devuelto final.  <br/> |
   
Durante las condiciones de error, los implementadores de los métodos de interfaz que necesite preste atención a los parámetros de salida y de entrada y salida debido a que el autor de la llamada normalmente no tiene ninguna forma de limpieza de ellos. Si se devuelve un error, a continuación, cada resultado o el parámetro de entrada y salida debe ser de izquierda en el valor inicializado el autor de la llamada o establecer en un valor que se puede limpiar sin ninguna acción por parte del autor de la llamada. Por ejemplo, un puntero-parámetro de salida de `void ** ppv` debe mantenerse tal como estaba en la entrada, o se puede establecer en NULL ( `*ppv = NULL`).
  

