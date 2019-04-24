---
title: Información sobre la resolución de conflictos para tipos de elementos personalizados
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: En este tema se describe cómo resolver conflictos de los tipos de elementos personalizados que se crean en Outlook.
ms.openlocfilehash: 357dd9182f26c4e9e1e264afdee296859e7b3483
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316950"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>Información sobre la resolución de conflictos para tipos de elementos personalizados

En este tema se describe cómo resolver conflictos de los tipos de elementos personalizados que se crean en Outlook.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Resolución de conflictos para tipos de elementos estándar de Outlook

En Outlook, los conflictos se producen cuando se han modificado dos o más copias del mismo elemento de forma independiente entre sí. Outlook detecta los conflictos durante la sincronización. Por ejemplo, puede actualizar un elemento de reunión en línea en Outlook Web App y, a continuación, actualizar el mismo elemento de reunión en Outlook cuando trabaje sin conexión. Cuando Outlook vuelve a estar en línea y sincroniza los datos entre el equipo cliente y el servidor, detecta que hay dos copias diferentes del mismo elemento de reunión.
  
Cuando Outlook sincroniza los elementos que pertenecen a un tipo de elemento de Outlook estándar, tiene en cuenta las propiedades que son específicas de ese tipo de elemento para detectar posibles conflictos. Outlook intenta resolver los conflictos y almacena la copia resultante en la carpeta correspondiente sin solicitar la intervención del usuario. En los casos en los que Outlook considere que existe la posibilidad de que la copia resultante no contenga todos los datos esenciales, Outlook almacena las copias conflictivas en la carpeta conflictos, en la carpeta problemas de sincronización. 
  
> [!NOTE]
> Problemas de sincronización y sus subcarpetas están ocultos hasta que haga clic en **lista de carpetas** en el panel de navegación. 
  
En estos casos, los usuarios pueden elegir ir a la carpeta conflictos para comprobar qué elementos estaban en conflicto y si usar una copia en la carpeta conflictos para reemplazar la copia que Outlook decidió conservar.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Resolución de conflictos para tipos de elementos personalizados

### <a name="item-types-and-message-classes"></a>Tipos de elemento y clases de mensaje
  
Todos los elementos de Outlook están asociados a una clase de mensaje. Por ejemplo, de forma predeterminada, un elemento de correo está asociado a la clase de mensaje **IPM. Nota**. La clase de mensaje se usa principalmente para identificar el formulario que se debe usar para mostrar el elemento en Outlook. Outlook admite una lista de clases de mensajes que se asignan a los tipos de elementos integrados en Outlook. Para más información sobre las clases de mensajes, vea [Tipos de elementos y clases de mensajes](https://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Los usuarios pueden crear tipos de elementos personalizados, asignar clases de mensaje personalizadas a los tipos de elemento personalizados y hacer que Outlook use un formulario personalizado para mostrar los tipos de elementos personalizados. Por ejemplo, es posible que desee que Outlook muestre un formulario de contacto profesional personalizado para los contactos profesionales. Para ello, puede crear una clase de mensaje personalizada **IPM. Contact. Business**, cree un formulario personalizado para esta clase de mensaje y asigne contactos profesionales con esta clase de mensaje. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Registro de un esquema de resolución de conflictos para tipos de elementos personalizados
  
Cuando se crea un tipo de elemento personalizado que no sea la clase de mensaje personalizada y el formulario personalizado, también se debe tener en cuenta cómo desea que Outlook controle los conflictos entre las copias de un elemento de este tipo de elemento. De forma predeterminada, Outlook emplea un esquema de resolución común a todos los elementos, no tiene en cuenta las propiedades que son específicas de un tipo de elemento y presenta las copias conflictivas para que el usuario tome una decisión. Esto se debe a que los tipos de elementos personalizados pueden definir campos personalizados en el formulario personalizado y pueden tener propiedades personalizadas y código personalizado. Si desea que Outlook considere las propiedades específicas del elemento e intente resolver el conflicto con una intervención mínima del usuario, debe especificarlo a través de una configuración en el registro de Windows. Esto se puede lograr de dos maneras: 
  
- Aplicando una configuración de directiva de grupo al equipo local que establece la clave del registro ConflictMsgCls. El siguiente ejemplo especifica la versión "14,0" para Outlook 2010: 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- Mediante la modificación directa de la clave del registro de usuario ConflictMsgCls. El siguiente ejemplo especifica la versión "14,0" para Outlook 2010: 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
La configuración de la resolución de conflictos mediante la Directiva de grupo tiene prioridad sobre la modificación directa de la clave del registro de usuario. La ubicación de la clave en el registro depende de la versión de Outlook. Especifique el nombre de la clase de mensaje personalizada como un valor en esta clave. Especifique el tipo de valor como **DWORD**y los datos del valor como uno de los valores que se muestran en la tabla siguiente, según el esquema de resolución que elija. 
  
|Datos  | Descripción  |
|:-----|:-----|
|comprendi  <br/> |Resolución de elementos comunes que requiere una decisión del usuario, tal y como se usa en Outlook 2002 y versiones anteriores.  <br/> |
|1  <br/> |Resolución de elementos comunes que requiere una intervención mínima del usuario, como se utiliza en Outlook desde Outlook 2003.  <br/> |
|segundo  <br/> |Resolución específica de los elementos de correo.  <br/> |
|3  <br/> |Resolución específica de los elementos de reunión.  <br/> |
|4  <br/> |Resolución específica de los elementos de cita.  <br/> |
|2,5  <br/> |Resolución específica de los elementos de contacto.  <br/> |
|6,5  <br/> |Resolución específica de los elementos de tarea.  <br/> |
|0,7  <br/> |Resolución específica de los elementos de notas rápidas.  <br/> |
|8,5  <br/> |Resolución específica de los elementos del diario.  <br/> |
   
Si especifica uno de los esquemas de resolución específicos de elementos (datos clave de 2 a 8), Outlook intentará resolver conflictos en campos específicos de elementos (por ejemplo, los campos de **Inicio** y **finalización** de un elemento de cita) automáticamente sin la intervención del usuario. . Si Outlook considera que la resolución puede dar como resultado la pérdida de datos esenciales, Outlook retendrá las copias conflictivas de la carpeta conflictos y los usuarios pueden elegir ir a la carpeta conflictos para volver a resolver estos elementos de forma manual y anular la operación automática n. 
  
Con el mismo ejemplo de contactos profesionales anterior, si desea especificar el esquema de resolución específico del elemento de contacto para la clase de mensaje personalizada **IPM. Contact. Business**, puede agregarlo como un valor **DWORD** en `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls`y especificar 5 como los datos. 
  
> [!NOTE]
> Outlook siempre usa un esquema de resolución específico de elementos de cita para clases de mensaje personalizadas que se basan en la clase de mensaje de cita, **IPM. Cita** (por ejemplo, **IPM. Appointment. personal**). 
  
## <a name="see-also"></a>Vea también

- [Objetos de elementos de Outlook](https://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

