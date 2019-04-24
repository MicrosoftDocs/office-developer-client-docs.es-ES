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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329704"
---
# <a name="using-a-table-to-work-with-properties"></a>Uso de una tabla para trabajar con propiedades

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Hay muchas propiedades disponibles tanto en los objetos que las admiten como en columnas en las tablas. Siempre que sea posible, recupere estas propiedades a través de la tabla.
  
Llame al [IMAPITable:: SetColumns](imapitable-setcolumns.md) para incluir todas las propiedades que necesita el cliente y el método [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas las filas de la tabla. 
  
Estas dos llamadas suelen ser suficientes para recuperar la información suficiente para mostrar a un usuario y son con frecuencia suficientes para cualquier procesamiento interno necesario, haciendo una llamada a **OpenEntry** para abrir el objeto innecesario. 
  
Solo hay dos excepciones:
  
- Si la propiedad es de más de 255 bytes. La interfaz * * IMAPITable * * puede que no devuelva el valor completo de la propiedad, en lugar de truncarla en 255 bytes. No obstante, piense en esta desventaja. Si va a mostrar estos datos al usuario, 255 bytes pueden ser suficientes para un campo de texto, como un comentario. 
    
- Si necesita una propiedad específica de una sola fila de una tabla. En este caso, no es necesario crear una tabla con propiedades que nunca se usarán. La mayoría de las veces, necesitará las mismas propiedades para todas las filas.
    

