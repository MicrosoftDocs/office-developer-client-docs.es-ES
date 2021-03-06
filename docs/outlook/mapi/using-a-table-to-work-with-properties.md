---
title: Uso de una tabla para trabajar con propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439915"
---
# <a name="using-a-table-to-work-with-properties"></a>Uso de una tabla para trabajar con propiedades

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchas propiedades están disponibles tanto desde los objetos que las admiten como como columnas en las tablas. Siempre que sea posible, recupere estas propiedades a través de la tabla.
  
Llama [a IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir todas las propiedades que el cliente necesita e [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar todas las filas de la tabla. 
  
Estas dos llamadas suelen ser suficientes para recuperar suficiente información para mostrar a un usuario y con frecuencia son suficientes para cualquier procesamiento interno necesario, por lo que una llamada a **OpenEntry** para abrir el objeto es innecesaria. 
  
Solo hay dos excepciones:
  
- Si la propiedad supera los 255 bytes. Es posible que la interfaz ** IMAPITable ** no devuelva el valor completo de la propiedad y, en su lugar, la trunca en 255 bytes. Sin embargo, piense en esta negociación. Si va a mostrar estos datos al usuario, es posible que 255 bytes sean suficientes para un campo textual como un comentario. 
    
- Si necesita una propiedad específica de una sola fila de una tabla. En este caso, no es necesario crear una tabla con propiedades que nunca se usarán. La mayoría de las veces necesitará las mismas propiedades para todas las filas.
    

