---
title: Outlook Interfaces de proveedor de Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: El Outlook Social Connector (OSC) es una característica de Office compartida por aplicaciones cliente de Office que se conecta a redes sociales y empresariales para que los usuarios puedan mantenerse en contacto con las personas de sus redes sin salir de Office.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422813"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Outlook Interfaces de proveedor de Social Connector

El Outlook Social Connector (OSC) es una característica de Office compartida por aplicaciones cliente de Office que se conecta a redes sociales y empresariales para que los usuarios puedan mantenerse en contacto con las personas de sus redes sin salir de Office. 
  
Un proveedor de OSC es un DLL del Modelo de objetos componentes (COM) que permite al OSC obtener acceso a los datos de redes sociales de forma independiente de las API de cada red social. En la tabla siguiente se enumeran las interfaces de extensibilidad del proveedor de OSC. Un proveedor de OSC debe implementar cuatro de las cinco interfaces para comunicarse con el OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)e [ISocialSession](isocialsessioniunknown.md). Si el proveedor de OSC admite actividades de sincronización, sincronización híbrida o a petición de amigos, almacenamiento en caché de credenciales de inicio de sesión e inicio de sesión con credenciales almacenadas en caché, o la capacidad de seguir a una persona, el proveedor también debe implementar [ISocialSession2.](isocialsession2iunknown.md)
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Representa a una persona en la red social.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Representa al usuario que ha iniciado sesión.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Representa una instancia de un proveedor de OSC.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Representa una conexión a un sitio de red social.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Admite la sincronización de actividades, la adición de amigos, la sincronización híbrida o a petición de los amigos o el inicio de sesión en la red social mediante credenciales almacenadas en caché.  <br/> |
   

