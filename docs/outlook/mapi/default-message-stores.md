---
title: Almacenes de mensaje predeterminado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576914"
---
# <a name="default-message-stores"></a>Almacenes de mensaje predeterminado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un almac�n de mensajes predeterminado es aquel que las aplicaciones de cliente pueden utilizar para tareas de mensajer�a de prop�sito general. Hay una serie de caracter�sticas opcionales para los proveedores de almac�n de mensajes que pasan a ser necesarios si el proveedor de almac�n de mensajes es que se utilizar� como almac�n de mensajes predeterminado. Son los siguientes:
  
- Implementaci�n de las carpetas especiales: las carpetas Bandeja de entrada, Bandeja de salida y los resultados de b�squeda.
    
- Proporcionar informes de lectura y nonread.
    
- Permitir env�os de mensajes entrantes y salientes.
    
- Permitir la creaci�n de mensajes con clases de mensaje arbitrario.
    
- Compatibilidad con las propiedades con nombre y varios valores.
    
- Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider. 
    
- Supporting associated contents tables. For more information, see [Tablas de contenido](contents-tables.md).
    
- Compatibilidad con notificaci�n de la cola MAPI cuando hay mensajes en la cola de mensajes salientes.
    
## <a name="see-also"></a>Vea tambi�n



[Desarrollar un proveedor de almac�n de mensajes de MAPI](developing-a-mapi-message-store-provider.md)

