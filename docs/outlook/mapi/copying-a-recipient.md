---
title: Copiar un destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3a4fb1a3f76481bf1960c251a33911b871a8791c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419089"
---
# <a name="copying-a-recipient"></a>Copiar un destinatario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para copiar uno o más destinatarios de un contenedor en otro o en el mismo contenedor, compruebe primero que el contenedor de destino es modificable. Los contenedores modificables establecen la marca AB_MODIFIABLE en su **PR_CONTAINER_FLAGS** propiedad ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)).
  
Para copiar una o más entradas en un contenedor modificable, llama al método [IABContainer::CopyEntries del](iabcontainer-copyentries.md) contenedor de destino. Dado que copiar entradas de la libreta de direcciones puede llevar mucho tiempo, **CopyEntries** acepta cuatro parámetros de entrada: una matriz de identificadores de entrada para las entradas que se van a copiar, un identificador de ventana, un indicador de progreso y una máscara de bits de marcas. 
  
El proveedor de libreta de direcciones usa el identificador de ventana y el indicador de progreso para mostrar el estado de la operación al usuario. Si desea mostrar el progreso, pase un identificador de ventana para la ventana principal del indicador de progreso en el parámetro _ulUIParam_ y no establezca la marca AB_NO_DIALOG en el parámetro _ulFlags._ Si tiene su propia implementación de un indicador de progreso, pase un puntero a la implementación en el parámetro _lpProgress._ Si no es así, pase NULL. El proveedor de libreta de direcciones usará la implementación del indicador de progreso MAPI. 
  
La máscara de bits de las marcas indica si desea mostrar o no un indicador de progreso y cómo debe controlarse la comprobación de entradas duplicadas. Establece la marca AB_NO_DIALOG para suprimir un indicador de progreso. Establezca la marca CREATE_CHECK_DUP_LOOSE para indicar al proveedor de libreta de direcciones que compruebe de forma flexible si hay duplicados o la marca CREATE_CHECK_DUP_STRICT para comprobar los duplicados de forma más estricta. Establezca la marca CREATE_REPLACE para que las entradas copiadas reemplacen las entradas existentes cuando el proveedor determine que hay duplicados. 
  
Al copiar en un contenedor de libreta de direcciones personal (PAB), el proveedor copia algunas o todas las propiedades de cada entrada. Dado que MAPI no establece requisitos para los proveedores que implementan operaciones de copia de contenedor, no puede hacer suposiciones sobre el número y el tipo de propiedades que se copian con una entrada de la libreta de direcciones.
  

