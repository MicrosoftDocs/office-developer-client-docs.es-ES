---
title: Interfaces de proveedor de Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) es una característica de Office compartida por las aplicaciones cliente de Office que se conecta a redes sociales y empresariales para que los usuarios puedan estar en contacto con las personas de sus redes sin salir de Office.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422813"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Interfaces de proveedor de Outlook Social Connector

Outlook Social Connector (OSC) es una característica de Office compartida por las aplicaciones cliente de Office que se conecta a redes sociales y empresariales para que los usuarios puedan estar en contacto con las personas de sus redes sin salir de Office. 
  
Un proveedor OSC es un archivo DLL del modelo de objetos componentes (COM) que permite al OSC tener acceso a los datos de la red social de manera independiente de las API de cada red social. En la siguiente tabla se enumeran las interfaces de la extensibilidad del proveedor de OSC. Un proveedor OSC debe implementar cuatro de las cinco interfaces para comunicarse con el OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)y [ISocialSession](isocialsessioniunknown.md). Si el proveedor de OSC admite la sincronización de actividades, la sincronización híbrida o a petición de amigos, el almacenamiento en caché de credenciales de inicio de sesión y el inicio de sesión con credenciales almacenadas en caché, o la posibilidad de seguir a una persona, el proveedor debe implementar [ISocialSession2 ](isocialsession2iunknown.md), también.
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Representa una persona de la red social.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Representa el usuario que ha iniciado sesión.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Representa una instancia de un proveedor de OSC.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Representa una conexión a un sitio de red social.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Admite la sincronización de actividades, la adición de amigos, la sincronización a petición o la sincronización híbrida de amigos o el inicio de sesión en la red social mediante el uso de credenciales almacenadas en caché.  <br/> |
   

