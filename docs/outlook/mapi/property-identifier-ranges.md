---
title: Intervalos de identificadores de propiedad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cdf1eae945cddf9eb76a2b7a2532d5dc6568beac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422708"
---
# <a name="property-identifier-ranges"></a>Intervalos de identificadores de propiedad

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En la tabla siguiente se resumen los distintos intervalos para los identificadores de propiedad, describiendo el propietario de las propiedades de cada intervalo.
  
|**Intervalo de identificadores**|**Descripción**|
|:-----|:-----|
|0000  <br/> |Reservado por MAPI para el valor especial **PR_NULL**.  <br/> |
|0001 - 0BFF  <br/> |Propiedades de sobre de mensaje definidas por MAPI.  <br/> |
|0C00 - 0DFF  <br/> |Propiedades de destinatario definidas por MAPI.  <br/> |
|0E00 - 0FFF  <br/> |Propiedades de mensaje no transmitibles definidas por MAPI.  <br/> |
|1000 - 2FFF  <br/> |Propiedades de contenido de mensajes definidas por MAPI.  <br/> |
|3000 - 3FFF  <br/> |Propiedades de objetos distintos de los mensajes y destinatarios definidos por MAPI.  <br/> |
|4000 - 57FF  <br/> |Propiedades de sobre de mensaje definidas por los proveedores de transporte.  <br/> |
|5800 - 5FFF  <br/> |Propiedades de destinatarios definidas por proveedores de transporte y libreta de direcciones.  <br/> |
|6000 - 65FF  <br/> |Propiedades de mensaje no transmitibles definidas por los clientes.  <br/> |
|6600 - 67FF  <br/> |Propiedades no transmitibles definidas por un proveedor de servicios. Estas propiedades pueden ser visibles o invisibles para los usuarios.  <br/> |
|6800 - 7BFF  <br/> |Propiedades de contenido de mensajes para clases de mensaje personalizadas definidas por los creadores de esas clases.  <br/> |
|7C00 - 7FFF  <br/> |Propiedades no transmitibles para clases de mensajes personalizadas definidas por los creadores de esas clases.  <br/> |
|8000 - FFFE  <br/> |Propiedades definidas por clientes y ocasionalmente proveedores de servicios que se identifican por nombre a través de los [métodos IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)  <br/> |
|FFFF  <br/> |Reservado por MAPI para el valor de error especial PROP_ID_INVALID.  <br/> |
   
El intervalo entre 3000 y 3FFF está reservado para las propiedades que no están relacionadas con mensajes o destinatarios. MAPI divide este rango en sub intervalos por tipos de objeto; en la tabla siguiente se muestra este desglose adicional. 
  
|**Intervalo de identificadores**|**Tipo de propiedad**|
|:-----|:-----|
|3000 - 33FF  <br/> |Propiedades comunes que aparecen en varios objetos, **como PR_DISPLAY_NAME** y **PR_ENTRYID**.  <br/> |
|3400 - 35FF  <br/> |Propiedades del almacén de mensajes  <br/> |
|3600 - 36FF  <br/> |Propiedades del contenedor de carpetas y libretas de direcciones  <br/> |
|3700 - 38FF  <br/> |Propiedades de datos adjuntos  <br/> |
|3900 - 39FF  <br/> |Propiedades de la libreta de direcciones  <br/> |
|3A00 - 3BFF  <br/> |Propiedades de usuario de mensajería  <br/> |
|3C00 - 3CFF  <br/> |Propiedades de la lista de distribución  <br/> |
|3D00 - 3DFF  <br/> |Propiedades de perfil  <br/> |
|3E00 - 3FFF  <br/> |Propiedades del objeto Status  <br/> |
   

