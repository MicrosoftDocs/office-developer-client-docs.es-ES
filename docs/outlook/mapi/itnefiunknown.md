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
ms.openlocfilehash: e8267b254648870cea4e16b4dea0e9c92e316fb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818012"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Proporciona métodos para encapsular las propiedades de MAPI que no son compatibles con un sistema de mensajería en secuencias binario que se pueden adjuntar a los mensajes. El formato utilizado para esta encapsulación es el formato de encapsulación neutro para el transporte (TNEF). El proveedor de transporte de destino o la aplicación de cliente basado en MAPI puede, a continuación, al recibir un mensaje que incluye datos adjuntos TNEF, recuperar las propiedades de los datos adjuntos.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |TNEF.h  <br/> |
|Expuestos por:  <br/> |Objetos TNEF  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace  <br/> |
|Identificador de interfaz:  <br/> |IID_ITNEF  <br/> |
|Tipo de puntero:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Permite que el proveedor de servicios de llamada o la puerta de enlace Agregar propiedades a la encapsulación de un mensaje o datos adjuntos.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Extrae las propiedades de una encapsulación TNEF.  <br/> |
|[Finish](itnef-finish.md) <br/> |Termina de procesamiento para todas las operaciones de TNEF que se ponen en cola y a la espera.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Se abre una interfaz de secuencia en el texto de un mensaje de encapsulado.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Establece el valor de una o más propiedades para un mensaje encapsulado o adjunto sin modificar el mensaje original o datos adjuntos.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Codifica una vista de tabla de destinatarios de un mensaje en la secuencia de datos TNEF para el mensaje.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Procesa los componentes individuales de un mensaje de uno a la vez en una secuencia TNEF.  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

