---
title: Almacenes de mensajes predeterminados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576914"
---
# <a name="default-message-stores"></a>Almacenes de mensajes predeterminados

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Un almacén de mensajes predeterminado es aquel que las aplicaciones cliente pueden usar para las tareas generales de mensajería. Hay varias características opcionales para los proveedores de almacenes de mensajes que pasan a ser necesarios si el proveedor del almacén de mensajes va a usarse como almacén de mensajes predeterminado. Son las siguientes:
  
- Implementar las carpetas especiales: las carpetas Bandeja de entrada, Bandeja de salida y resultados de búsqueda.
    
- Proporcionar informes de lectura y nonread.
    
- Permitir envíos de mensajes entrantes y salientes.
    
- Permitir la creación de mensajes con clases de mensaje arbitrario.
    
- Compatibilidad con las propiedades con nombre y varios valores.
    
- Compatibilidad con el método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md), incluso si el proveedor del almacén de mensajes está estrechamente acoplado a un proveedor de transporte. 
    
- Compatibilidad con tablas de contenido asociadas. Para obtener más información, vea [Tablas de contenido](contents-tables.md).
    
- Compatibilidad con la notificación de la cola MAPI cuando hay mensajes en la cola de mensajes salientes.
    
## <a name="see-also"></a>Vea también



[Desarrollar un proveedor de almacén de mensajes MAPI](developing-a-mapi-message-store-provider.md)

