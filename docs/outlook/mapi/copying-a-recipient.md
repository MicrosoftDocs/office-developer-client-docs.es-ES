---
title: Copiar un destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: dd68bc2054136a7f587b05dc56dbeabd06de1f08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816590"
---
# <a name="copying-a-recipient"></a>Copiar un destinatario

  
  
**Se aplica a**: Outlook 
  
Para copiar a uno o más destinatarios de un contenedor a otro o el mismo contenedor, compruebe primero que el contenedor de destino es modificable. Contenedores que son modificables establecen la marca AB_MODIFIABLE en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)).
  
Para copiar una o varias entradas en un contenedor modificable, llame al método [IABContainer::CopyEntries](iabcontainer-copyentries.md) del contenedor de destino. Debido a que puede llevar mucho tiempo copiar entradas de la libreta de direcciones, **CopyEntries** acepta cuatro parámetros de entrada: una matriz de identificadores de entrada para las entradas que se va a copiar, un identificador de ventana, un indicador de progreso y una máscara de bits de indicadores. 
  
El indicador de progreso y de controlador de ventana usadas por el proveedor de la libreta de direcciones para mostrar el estado de la operación al usuario. Si desea mostrar el progreso, pasar un identificador de ventana para la ventana principal del indicador de progreso en el parámetro _ulUIParam_ y no se establece la marca AB_NO_DIALOG en el parámetro _ulFlags indicado_ . Si tiene su propia implementación de un indicador de progreso, pase un puntero a la implementación en el parámetro _lpProgress_ . En caso contrario, pase el valor NULL. El proveedor de la libreta de direcciones utilizará la implementación de indicador de progreso MAPI. 
  
La máscara de bits de indicadores indica si va a mostrar un indicador de progreso y entrada duplicado cómo deben controlarse de comprobación. Establecer la marca AB_NO_DIALOG para suprimir un indicador de progreso. Establecer el indicador CREATE_CHECK_DUP_LOOSE para indicar a la libreta de direcciones para buscar escasamente duplicados o el indicador CREATE_CHECK_DUP_STRICT para la comprobación duplicada más estrictas. Establece el indicador CREATE_REPLACE que ha copiado las entradas se reemplazan las entradas existentes cuando el proveedor determina que hay duplicados. 
  
Cuando se copian en un contenedor de libreta personal de direcciones, el proveedor de copia algunas o todas las propiedades para cada entrada. Debido a que MAPI no establecer requisitos para los proveedores que implementan las operaciones de copia de contenedor, puede hacer suposiciones sobre el número y el tipo de las propiedades que se copian con una entrada de la libreta de direcciones.
  

