---
title: Acerca de la resolución de conflictos para tipos de elemento personalizado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: En este tema se describe cómo resolver los conflictos de tipos de elemento personalizadas que se crean en Outlook.
ms.openlocfilehash: d85c2022d909901c71c20214f91b316cce81c596
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816042"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>Acerca de la resolución de conflictos para tipos de elemento personalizado

En este tema se describe cómo resolver los conflictos de tipos de elemento personalizadas que se crean en Outlook.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Resolución de conflictos para tipos de elemento de Outlook estándar

En Outlook, se producen conflictos cuando dos o más copias del mismo elemento se han modificado independientemente de los demás. Outlook detecta conflictos durante la sincronización. Por ejemplo, es posible que actualizar un elemento de reunión en línea en Outlook Web App y, a continuación, actualice el mismo elemento de reunión en Outlook cuando se trabaja sin conexión. Cuando Outlook pasa vuelva a estar en línea y sincroniza los datos entre el equipo cliente y el servidor, detecta que hay dos copias diferentes del mismo elemento de reunión.
  
Cuando Outlook sincroniza los elementos que pertenecen a un tipo de elemento de Outlook estándar, tiene en cuenta las propiedades que son específicas para ese tipo de elemento para detectar posibles conflictos. Outlook intenta resolver conflictos y almacena la copia resultante en la carpeta correspondiente sin solicitar la intervención del usuario. En los casos donde Outlook considera que existe la posibilidad de que la copia resultante no puede contener todos los datos esenciales, Outlook almacena las copias en la carpeta conflictos, bajo la carpeta problemas de sincronización en conflicto. 
  
> [!NOTE]
> Problemas de sincronización y sus subcarpetas están ocultos hasta que haga clic en **Lista de carpetas** en el panel de navegación. 
  
En estos casos, los usuarios pueden elegir ir a la carpeta conflictos para comprobar qué elementos se encontraban en conflicto y si se debe utilizar una copia de la carpeta conflictos para reemplazar la copia que Outlook ha decidido conservar.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Resolución de conflictos para tipos de elemento personalizado

### <a name="item-types-and-message-classes"></a>Tipos de elementos y clases de mensajes
  
Todos los elementos de Outlook están asociados con una clase de mensaje. Por ejemplo, de forma predeterminada, un elemento de correo está asociado con la clase de mensaje IPM **. Nota**. La clase de mensaje se usa principalmente para identificar el formulario que debe usarse para mostrar el elemento de Outlook. Outlook es compatible con una lista de las clases de mensajes que se asignan a los tipos de elementos que se integra en Outlook. Para más información sobre las clases de mensajes, vea [Tipos de elementos y clases de mensajes](http://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Los usuarios pueden crear tipos de elemento personalizado, asignar clases de mensaje personalizadas a los tipos de elemento personalizado y que Outlook utilice un formulario personalizado para mostrar los tipos de elemento personalizado. Por ejemplo, puede ser conveniente para mostrar un formulario de contacto de negocio personalizado para los contactos profesionales de Outlook. Para ello, puede crear una clase de mensaje personalizada **IPM. Contact.Business**, crear un formulario personalizado para esta clase de mensaje y asignar contactos profesionales con esta clase de mensaje. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Registrar un esquema de resolución de conflicto para tipos de elemento personalizado
  
Cuando se crea un tipo de elemento personalizado, que no sea la clase de mensaje personalizada y un formulario personalizado, también debe tener en cuenta cómo le gustaría que Outlook para controlar conflictos entre las copias de un elemento de este tipo de elemento. De forma predeterminada, Outlook emplea un esquema de resolución comunes a todos los elementos, no tiene en cuenta las propiedades que son específicas de un tipo de elemento y presenta copias en conflicto para el usuario tomar una decisión. Esto es debido a que los tipos de elemento personalizado pueden definir los campos personalizados en el formulario personalizado y pueden tener propiedades personalizadas y código personalizado. Si desea que Outlook a tener en cuenta las propiedades específicas del elemento e intente resolver el conflicto con mínima intervención del usuario, debe especificar a través de una opción de configuración en el registro de Windows. Esto se puede lograr de una de dos maneras: 
  
- Aplicando una configuración de directiva de grupo en el equipo local establece la clave del registro ConflictMsgCls. En el ejemplo siguiente se especifica la versión "14.0" para Outlook 2010: 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- Al modificar directamente la clave del registro de usuario ConflictMsgCls. En el ejemplo siguiente se especifica la versión "14.0" para Outlook 2010: 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
Configuración de la resolución de conflictos a través de la directiva de grupo tiene prioridad sobre modificar directamente la clave del registro de usuario. La ubicación de la clave en el registro depende de la versión de Outlook. Especifique el nombre de la clase de mensaje personalizada como un valor bajo esta clave. Especifique el tipo del valor como **DWORD**y los datos del valor como uno de los valores que se muestran en la tabla siguiente, según el esquema de resolución que elija. 
  
|Datos  | Descripción  |
|:-----|:-----|
|0  <br/> |Resolución de elemento común que requiere una decisión del usuario, como se utiliza en Outlook 2002 y versiones anteriores.  <br/> |
|1  <br/> |Resolución de elemento común que requiere la intervención mínima del usuario, como se utiliza en Outlook desde Outlook 2003.  <br/> |
|2  <br/> |Resolución específica de elementos de correo.  <br/> |
|3  <br/> |Resolución específico a los elementos de la reunión.  <br/> |
|4  <br/> |Resolución específica de elementos de cita.  <br/> |
|5  <br/> |Resolución específico para elementos de contacto.  <br/> |
|6  <br/> |Resolución específica de elementos de tarea.  <br/> |
|7  <br/> |Resolución específica a los elementos de la nota.  <br/> |
|8  <br/> |Resolución específica para los elementos del diario.  <br/> |
   
Si especifica uno de los esquemas de resolución específicos de un elemento (datos clave 2 al 8), Outlook intenta resolver conflictos en campos específicos de un elemento (por ejemplo, campos de **comienzo** y **final** de un elemento de cita) automáticamente sin la intervención del usuario . Si Outlook se considera que la solución puede producir la pérdida de datos esenciales, Outlook mantendrá copias en conflicto en la carpeta conflictos y los usuarios pueden elegir ir a la carpeta conflictos para volver a resolver estos elementos de forma manual y reemplazar el automático resolución. 
  
Utilizando el mismo ejemplo de los contactos de negocio anterior, si desea especificar el esquema de resolución de específicos de un elemento de contacto para la clase de mensaje personalizada **IPM. Contact.Business**, puede agregarlo como un valor **DWORD** en `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls`y especificar 5 como los datos. 
  
> [!NOTE]
> Outlook siempre utiliza un esquema de resolución que es específico de elementos de cita para las clases de mensaje personalizado que se basan en la clase de mensaje de cita, **IPM. Cita** (por ejemplo, **IPM. Appointment.Personal**). 
  
## <a name="see-also"></a>Ver también

- [Objetos de elementos de Outlook](http://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

