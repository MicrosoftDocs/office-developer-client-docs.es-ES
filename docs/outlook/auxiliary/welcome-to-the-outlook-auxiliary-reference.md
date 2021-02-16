---
title: Referencia auxiliar de Outlook
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: La referencia auxiliar de Outlook contiene contenido conceptual y documentación de referencia para cuatro conjuntos de API, ejemplos de código y un instalador redistribuible que permite a los desarrolladores ampliar e integrarse con Outlook. Outlook expone las API de esta referencia para su extensibilidad, fuera del modelo de objetos de Outlook.
ms.openlocfilehash: 445d35c12e4c8984d47adcef3ecf50ebd881875b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328991"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Referencia auxiliar de Outlook

La referencia auxiliar de Outlook contiene contenido conceptual y documentación de referencia para cuatro conjuntos de API, ejemplos de código y un instalador redistribuible que permite a los desarrolladores ampliar e integrarse con Outlook. Outlook expone las API de esta referencia para su extensibilidad, fuera del modelo de objetos de Outlook. 
  
Si no tiene experiencia en el desarrollo de soluciones para Outlook, consulte [Seleccionar una API o tecnología para desarrollar soluciones de Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) para identificar las API y tecnologías más adecuadas para sus necesidades. 

Para obtener información específica acerca del modelo de objetos de Outlook, vea la referencia [de VBA de Outlook.](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) 

Para obtener información específica acerca de la API de mensajería (MAPI) compatible con Outlook, vea la referencia [MAPI de Outlook](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx).

## <a name="conceptual"></a>Conceptual 

La discusión conceptual incluye los siguientes temas:
  
- [Acerca de la configuración de bloqueo de correo basura](about-anti-spam-settings.md)
    
- [Administrar la descarga de mensajes de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md)
    
- [Localizar el historial de descarga de mensajes de una cuenta POP3](locating-the-message-download-history-for-a-pop3-account.md)
    
- [Analizar el historial de descarga de mensajes de una cuenta POP3](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [Información sobre la resolución de conflictos para tipos de elementos personalizados](about-conflict-resolution-for-custom-item-types.md)
    
- [Acerca de la última hora de actualización de una libreta de direcciones sin conexión](about-the-last-update-time-of-an-offline-address-book.md)
    
- [Información sobre cómo registrar un nuevo dominio para la configuración automática](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [Acerca de las convocatorias de reunión como actualizaciones informativas y completa](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- Acerca de la redistribución de [calendarios](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) mediante programación para el horario de verano (también hay un instalador redistribuible para herramientas de reasalción de calendarios de terceros, que también funciona para versiones anteriores de Outlook, desde Outlook 2010. Para descargar el instalador, vea [Outlook 2010:](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)Instalador redistribuible de referencia auxiliar y archivo de encabezado para cambiar el tamaño de los calendarios).
    
- [Información sobre TZDEFINITION persistente en una secuencia para confirmar una propiedad binaria](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Referencia

El contenido de referencia incluye lo siguiente:
  
- Las [API exportadas por Outlook](about-apis-exported-by-outlook.md) incluyen funciones y estructuras de datos que se implementaron originalmente para uso interno y ahora se exponen para uso público. 
    
- La [API de administración de](about-the-account-management-api.md) cuentas proporciona acceso a la información de la cuenta de usuario y las notificaciones de los cambios en la cuenta. 
    
- La [API de capa de degradación](about-the-data-degradation-layer-api.md) de datos admite clientes que tienen acceso a un elemento de Outlook en un formato de carácter preferido en lugar del formato de carácter nativo del objeto. 
    
- La [API de disponibilidad proporciona](about-the-free-busy-api.md) información de estado de disponibilidad sobre cuentas de usuario específicas dentro de un intervalo de tiempo específico. 

## <a name="sample-tasks"></a>Tareas de muestra

Entre las tareas de procedimientos de ejemplo de la referencia auxiliar de Outlook se incluyen las siguientes:
    
- [Determinar si un elemento de Outlook se ha modificado pero no guardado (referencia auxiliar de Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [Analizar una secuencia de una propiedad binaria para leer la estructura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Analizar una secuencia de una propiedad binaria para leer la estructura TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Leer las propiedades de la zona horaria en una cita](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Especificar si se debe mostrar la imagen de un contacto en Outlook (referencia auxiliar de Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [Utilizar un tiempo relativo a los datos de disponibilidad de acceso](how-to-use-relative-time-to-access-free-busy-data.md)
    
La referencia de cada API enumera las constantes, definiciones de tipo e interfaces que un desarrollador debe implementar para usar la funcionalidad adicional.
  
> [!NOTE]
> Los desarrolladores deben implementar estas API solo como se documenta en esta referencia. Algunos miembros de la interfaz y parámetros de método se denominan marcadores de posición porque están reservados para el uso interno de Outlook y están sujetos a cambios sin previo aviso. 
  

