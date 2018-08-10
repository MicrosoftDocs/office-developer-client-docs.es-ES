---
title: Interfaces del proveedor de Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) es una característica de Office compartida por las aplicaciones cliente de Office que se conecta a sociales y las redes empresariales por lo que los usuarios pueden permanecer en contacto con las personas en sus redes sin salir de Office.
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821210"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Interfaces del proveedor de Outlook Social Connector

Outlook Social Connector (OSC) es una característica de Office compartida por las aplicaciones cliente de Office que se conecta a sociales y las redes empresariales por lo que los usuarios pueden permanecer en contacto con las personas en sus redes sin salir de Office. 
  
Un proveedor de OSC es un archivo DLL que permite el OSC tener acceso a datos de redes sociales de una forma que es independiente de la API de cada red social del modelo de objetos de componentes (COM). En la siguiente tabla se enumera las interfaces de extensibilidad del proveedor OSC. Debe implementar un proveedor de OSC cuatro de las cinco interfaces para comunicarse con el OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)y [ISocialSession](isocialsessioniunknown.md). Si el proveedor de OSC admite la sincronización de actividades, y a petición o sincronización híbrido de amigos, almacenamiento en caché las credenciales de inicio de sesión y registro uso en caché las credenciales o la capacidad que se deben seguir a una persona, el proveedor debe implementar [ISocialSession2 ](isocialsession2iunknown.md), así como.
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Representa a una persona en la red social.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Representa el usuario ha iniciado la sesión.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Representa una instancia de un proveedor de OSC.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Representa una conexión a un sitio de red social.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Admite la sincronización de actividades, adición de amigos, sincronización a petición o híbrido de amigos o inicie sesión en la red social mediante el uso de credenciales almacenadas en caché.  <br/> |
   

