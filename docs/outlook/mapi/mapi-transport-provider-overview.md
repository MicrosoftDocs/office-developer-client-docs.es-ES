---
title: Información general sobre el proveedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404578"
---
# <a name="mapi-transport-provider-overview"></a>Información general sobre el proveedor de transporte MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de transporte controlan la transmisión y recepción de mensajes e implementan la seguridad, si es necesario. También se encargan de las tareas necesarias de preprocesamiento y posprocesamiento. Normalmente hay un proveedor de transporte para cada sistema de mensajería activo.
  
Las aplicaciones cliente se comunican con el proveedor de transporte a través de un proveedor de almacenamiento de mensajes. 
  
Los proveedores de transporte se registran con MAPI para controlar uno o más tipos concretos de entradas de destinatario. Cuando un mensaje está listo para enviarse, MAPI debe determinar qué proveedor de transporte debe controlar la transmisión. Según el tipo de destinatario, MAPI puede incluso llamar a más de un proveedor de transporte. Si un proveedor de transporte no disponible es el único que puede controlar el destinatario, la transmisión de mensajes se pospondrá hasta que se pueda restablecer una conexión con ese proveedor.
  
Algunos sistemas de mensajería son sistemas seguros; todos los usuarios potenciales deben escribir un conjunto de credenciales válidas antes de permitir el acceso. MAPI impide el acceso no autorizado a estos sistemas de mensajería seguros haciendo que el proveedor de transporte valide las credenciales en el momento de iniciar sesión. 
  

