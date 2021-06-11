---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428518"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona métodos para encapsular propiedades MAPI que no son compatibles con un sistema de mensajería en secuencias binarias que se pueden adjuntar a los mensajes. El formato usado para esta encapsulación es el Transport-Neutral de encapsulación (TNEF). A continuación, el proveedor de transporte de destino o la aplicación cliente basada en MAPI pueden, al recibir un mensaje que incluye datos adjuntos de TNEF, recuperar las propiedades de los datos adjuntos.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Tnef.h  <br/> |
|Expuesto por:  <br/> |Objetos TNEF  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de transporte, proveedores de almacén de mensajes y puertas de enlace  <br/> |
|Identificador de interfaz:  <br/> |IID_ITNEF  <br/> |
|Tipo de puntero:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Permite al proveedor de servicios de llamadas o puerta de enlace agregar propiedades a la encapsulación de un mensaje o datos adjuntos.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Extrae las propiedades de una encapsulación TNEF.  <br/> |
|[Finish](itnef-finish.md) <br/> |Finaliza el procesamiento de todas las operaciones TNEF que están en cola y en espera.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Abre una interfaz de secuencia en el texto de un mensaje encapsulado.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Establece el valor de una o más propiedades para un mensaje encapsulado o datos adjuntos sin modificar el mensaje o los datos adjuntos originales.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Codifica una vista de la tabla de destinatarios de un mensaje en la secuencia de datos TNEF del mensaje.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Procesa componentes individuales de un mensaje uno a uno en una secuencia de TNEF.  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

