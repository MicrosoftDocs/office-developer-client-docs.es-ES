---
title: Rangos de identificador de propiedad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 479e5abda9137ddaedcabb8d914bc038ddf200f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581107"
---
# <a name="property-identifier-ranges"></a>Rangos de identificador de propiedad

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En la siguiente tabla se resume los intervalos diferentes para los identificadores de propiedad, que describe el propietario de las propiedades de cada intervalo.
  
|**Intervalo de identificadores de**|**Descripción**|
|:-----|:-----|
|0000  <br/> |Reservado por MAPI para el valor especial **PR_NULL**.  <br/> |
|0001 - 0BFF  <br/> |Propiedades sobre de mensaje definidas por MAPI.  <br/> |
|0C 00 - 0DFF  <br/> |Propiedades de destinatarios definidas por MAPI.  <br/> |
|0E00 - 0FFF  <br/> |Propiedades del mensaje no transmisible definidas por MAPI.  <br/> |
|1000 - 2FFF  <br/> |Propiedades de contenido de mensaje definidas por MAPI.  <br/> |
|3000 - 3FFF  <br/> |Propiedades de objetos que no sean mensajes y destinatarios definidos por MAPI.  <br/> |
|4000 - 57FF  <br/> |Propiedades sobre de mensaje definidas por los proveedores de transporte.  <br/> |
|5800 - 5FFF  <br/> |Propiedades de destinatarios definidas por los proveedores de libreta de direcciones y de transporte.  <br/> |
|6000 - 65FF  <br/> |Propiedades del mensaje no transmisible definidas por los clientes.  <br/> |
|6600 - 67FF  <br/> |Propiedades no transmisible definidas por un proveedor de servicios. Estas propiedades pueden ser visible o invisible a los usuarios.  <br/> |
|6800 - 7BFF  <br/> |Propiedades de contenido de mensaje para las clases de mensaje personalizadas definidas por los creadores de esas clases.  <br/> |
|7C 00 - 7FFF  <br/> |Propiedades no transmisible de clases de mensaje personalizadas definidas por los creadores de esas clases.  <br/> |
|8000 - FFFE  <br/> |Propiedades definidas por los clientes y proveedores que se identifican por su nombre a través de los métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) y [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) de servicios de cada cierto tiempo.  <br/> |
|FFFF  <br/> |Reservado por MAPI para el valor de error especiales PROP_ID_INVALID.  <br/> |
   
El intervalo entre 3000 y 3FFF está reservado para las propiedades que no están relacionadas con los mensajes o los destinatarios. MAPI divide este intervalo en intervalos subcaracterística por tipos de objeto; en la tabla siguiente se muestra este detalle adicional. 
  
|**Intervalo de identificadores de**|**Tipo de propiedad**|
|:-----|:-----|
|3000 - 33FF  <br/> |Propiedades comunes que aparecen en varios objetos, como **PR_DISPLAY_NAME** y la **entrada del objeto**.  <br/> |
|3400 - 35FF  <br/> |Propiedades de almacén de mensajes  <br/> |
|3600 - 36FF  <br/> |Carpeta y libreta de direcciones las propiedades del contenedor  <br/> |
|3700 - 38FF  <br/> |Propiedades de datos adjuntos  <br/> |
|3900 - 39FF  <br/> |Propiedades de la libreta de direcciones  <br/> |
|3A00 - 3BFF  <br/> |Las propiedades de usuario de mensajería  <br/> |
|3C 00 - 3CFF  <br/> |Propiedades de la lista de distribución  <br/> |
|3D 00 - 3DFF  <br/> |Propiedades de perfil  <br/> |
|3E00 - 3FFF  <br/> |Propiedades del objeto de estado  <br/> |
   

