---
title: Usar una tabla para trabajar con propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9f02da9eb1920f55acf65dfb6a503e42d4c3daf2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585426"
---
# <a name="using-a-table-to-work-with-properties"></a>Usar una tabla para trabajar con propiedades

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchas propiedades están disponibles desde los objetos que los admiten tanto como columnas en las tablas. Siempre que sea posible, recuperar estas propiedades a través de la tabla.
  
Llamar a [IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir todas las propiedades que necesita el cliente y [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas las filas de la tabla. 
  
Estos dos llamadas normalmente son suficientes para recuperar la información suficiente para mostrar a un usuario y con frecuencia suficientes para cualquier procesamiento interno necesario, realizar una llamada a **OpenEntry** para abrir el objeto innecesario. 
  
Hay sólo dos excepciones:
  
- Si la propiedad es más de 255 bytes. El ** IMAPITable ** interfaz no puede devolver el valor de propiedad completa, en su lugar el truncamiento a 255 bytes. Piense en este equilibrio, aunque. Si va a mostrar estos datos al usuario, 255 bytes puede ser suficiente para un campo de texto, como un comentario. 
    
- Si necesita una propiedad concreta de una sola fila de una tabla. En este caso no es necesario crear una tabla con las propiedades que nunca se va a usar. La mayor parte del tiempo, necesitará las mismas propiedades para todas las filas.
    

