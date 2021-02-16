---
title: Características del almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 092cf56aea2e246fbb7ef2016a2662a1f67f889b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439523"
---
# <a name="message-store-features"></a>Características del almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de almacenamiento de mensajes son más complejos que otros proveedores de servicios MAPI en que los proveedores de al almacenamiento de mensajes tienen una gama más amplia de características opcionales que pueden implementar. La lista de características necesarias para un proveedor de al almacenamiento de mensajes es bastante corta. Sin embargo, un proveedor de almacenamiento de mensajes típico admitirá varias características opcionales, ya que muchas de las características opcionales son muy útiles o son necesarias para la mayoría de los clientes MAPI. En la tabla siguiente se enumeran las características principales que los proveedores de al almacenamiento de mensajes pueden implementar y si cada característica es obligatoria u opcional para todos los proveedores de al almacenamiento de mensajes y para los proveedores de al almacenamiento de mensajes predeterminados.
  
|**Característica**|**Todo**|**Default**|
|:-----|:-----|:-----|
|Proporcionar estado con la tabla de estado MAPI.  <br/> |Obligatorio  <br/> |Obligatorio  <br/> |
|Implementar objetos de carpeta.  <br/> |Obligatorio  <br/> |Obligatorio  <br/> |
|Implementar objetos de mensaje.  <br/> |Obligatorio  <br/> |Obligatorio  <br/> |
|Proporcionar informes de lectura y nonread.  <br/> |Obligatorio  <br/> |Obligatorio  <br/> |
|Proporcionar una interfaz de progreso.  <br/> |Obligatorio  <br/> |Obligatorio  <br/> |
|Proporcionar una interfaz de configuración.  <br/> |Obligatorio  <br/> |Obligatorio  <br/> |
|Compatibilidad con tablas de contenido asociadas para la compatibilidad con formularios y vistas.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Enviar mensajes con el proveedor del almacén de mensajes.  <br/> |Opcional  <br/> |Obligatorio  <br/> |
|Recibir mensajes con el proveedor del almacén de mensajes.  <br/> |Opcional  <br/> |Obligatorio  <br/> |
|Compatibilidad con datos adjuntos de mensajes.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Compatibilidad con formato de texto enriquecido para mensajes.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Proporcionar notificaciones.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Admitir búsquedas.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Compatibilidad con proveedores de almacenamiento y transporte de mensajes estrechamente acoplados.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Admitir la no reutilización de identificadores de entrada.  <br/> |Opcional  <br/> |Opcional  <br/> |
   
Muchas de las características opcionales se pueden anunciar a MAPI y aplicaciones cliente estableciendo varias marcas en la propiedad PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)del objeto del almacén de mensajes. Las características necesarias no tienen marcas asociadas. **PR_STORE_SUPPORT_MASK** se requiere en el almacén de mensajes, la carpeta y los objetos del mensaje. 
  
## <a name="see-also"></a>Vea también



[Desarrollar un proveedor de almacén de mensajes MAPI](developing-a-mapi-message-store-provider.md)

