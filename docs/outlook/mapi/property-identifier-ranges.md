---
title: Intervalos de identificador de propiedad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cdf1eae945cddf9eb76a2b7a2532d5dc6568beac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328535"
---
# <a name="property-identifier-ranges"></a>Intervalos de identificador de propiedad

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
En la tabla siguiente se resumen los distintos intervalos para los identificadores de propiedad, que describen el propietario de las propiedades de cada intervalo.
  
|**Intervalo de identificadores**|**Descripción**|
|:-----|:-----|
|1,0000  <br/> |Reservado por MAPI para el valor especial **PR_NULL**.  <br/> |
|0001-0BFF  <br/> |Propiedades del sobre del mensaje definidas por MAPI.  <br/> |
|0C00-0DFF  <br/> |Propiedades de destinatarios definidas por MAPI.  <br/> |
|0E00-0FFF  <br/> |Propiedades de mensaje no transmitibles definidas por MAPI.  <br/> |
|1000-2FFF  <br/> |Propiedades de contenido de mensajes definidas por MAPI.  <br/> |
|3000-3FFF  <br/> |Propiedades de objetos que no sean mensajes y destinatarios definidos por MAPI.  <br/> |
|4000-57FF  <br/> |Propiedades del sobre del mensaje definidas por los proveedores de transporte.  <br/> |
|5800-5FFF  <br/> |Propiedades de destinatarios definidas por los proveedores de la libreta de direcciones y transporte.  <br/> |
|6000-65FF  <br/> |Propiedades de mensaje no transmitibles definidas por los clientes.  <br/> |
|6600-67FF  <br/> |Propiedades no transmitibles definidas por un proveedor de servicios. Estas propiedades pueden ser visibles o invisibles para los usuarios.  <br/> |
|6800-7BFF  <br/> |Propiedades de contenido de mensajes para clases de mensaje personalizadas definidas por creadores de esas clases.  <br/> |
|7C00-7FFF  <br/> |Propiedades que no se transmiten para las clases de mensaje personalizadas definidas por los creadores de esas clases.  <br/> |
|8000-FFFE  <br/> |Propiedades definidas por los clientes y ocasionalmente proveedores de servicios que se identifican por nombre a través de los métodos [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) y [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .  <br/> |
|FFFF  <br/> |Reservado por MAPI para el valor de error especial PROP_ID_INVALID.  <br/> |
   
El intervalo entre 3000 y 3FFF está reservado para las propiedades que no están relacionadas con los mensajes o los destinatarios. MAPI divide este intervalo en subrangos por tipos de objeto; en la tabla siguiente se muestra este desglose. 
  
|**Intervalo de identificadores**|**Tipo de propiedad**|
|:-----|:-----|
|3000-33FF  <br/> |Propiedades comunes que aparecen en varios objetos, como **PR_DISPLAY_NAME** y ****  <br/> |
|3400-35FF  <br/> |Propiedades del almacén de mensajes  <br/> |
|3600-36FF  <br/> |Propiedades del contenedor de la libreta de direcciones y carpetas  <br/> |
|3700-38FF  <br/> |Propiedades de datos adJuntos  <br/> |
|3900-39FF  <br/> |Propiedades de la libreta de direcciones  <br/> |
|3A00-3BFF  <br/> |Propiedades de usuario de mensajería  <br/> |
|3C00-3CFF  <br/> |Propiedades de la lista de distribución  <br/> |
|3D00-3DFF  <br/> |Propiedades de perfil  <br/> |
|3E00-3FFF  <br/> |Propiedades del objeto status  <br/> |
   

