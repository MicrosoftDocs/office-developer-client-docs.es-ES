---
title: Publicar formularios con código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Cualquier administrador de la colección de sitios puede publicar formularios con código directamente desde el Asistente para publicación de InfoPath Designer en una biblioteca de formularios en SharePoint. El código se ejecuta en un entorno de espacio aislado para que los códigos malintencionados no puedan dañar el servidor. Esto se denomina publicación de una solución de espacio aislado o publicación en la infraestructura de espacio aislado de SharePoint.
ms.openlocfilehash: f8f8a48ea6810b5331198f6ddc112b3bd38ab886
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428329"
---
# <a name="publishing-forms-with-code"></a>Publicar formularios con código

Cualquier administrador de la colección de sitios puede publicar formularios con código directamente desde el Asistente para publicación de InfoPath Designer en una biblioteca de formularios en SharePoint. El código se ejecuta en un entorno de espacio aislado para que los códigos malintencionados no puedan dañar el servidor. Esto se denomina publicación de una solución de espacio aislado o publicación en la infraestructura de espacio aislado de SharePoint.
  
InfoPath 2010 y SharePoint Server 2010 también admiten soluciones implementadas por el administrador. Un diseñador de formularios publica formularios con código en un almacén local y después un administrador de la granja de SharePoint los revisa y carga. El código es de plena confianza y puede incorporar funcionalidad que requiere privilegios elevados como E/S de archivo.
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a>Comparar soluciones de espacio aislado y aprobadas por administrador

La tabla siguiente resume las diferencias entre la publicación de soluciones de espacio aislado y aprobadas por el administrador. 
  
||**Soluciones de espacio aislado**|**Soluciones aprobadas por el administrador**|
|:-----|:-----|:-----|
|**Permisos requeridos** <br/> |Pueden ser publicadas por cualquier administrador de colección de sitios.  <br/> |Pueden ser implementadas por un administrador de granjas.  <br/> |
|**Publicación** <br/> |Se puede publicar directamente desde InfoPath.  <br/> |Pueden ser implementadas con una herramienta de Administración central o de línea de comandos stsadm.  <br/> |
|**Protection** <br/> |El código se ejecuta en un entorno de espacio aislado. Esto ayuda a proteger el servidor contra códigos malintencionados.  <br/> |El código puede ejecutarse con plena confianza y tener acceso a cualquier recurso del servidor.  <br/> |
|**Uso recomendado** <br/> |Formularios que solo requieren una pequeña cantidad de códigos.  <br/> |Formularios que contienen varias líneas de código.  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a>Publicación desde plantillas de formulario como soluciones de espacio aislado

La publicación de un formulario con código como una solución de espacio aislado no difiere de la publicación de cualquier otro formulario en una biblioteca de documentos. Simplemente se debe usar al asistente para publicación como se hace habitualmente y el formulario se cargará en el servidor y funcionará en el espacio aislado.
  
Tenga en cuenta que existen algunas restricciones para la implementación del formulario como una solución de espacio aislado:
  
- Debe ser un formulario de InfoPath.
    
- Debe usarse C# o Visual Basic como lenguaje de programación.
    
- No se pueden enviar a conexiones de datos de correo electrónico.
    
- No puede tener propiedades promovidas por conexiones parte a parte.
    
- No se debe tener ningún control de metadatos ni conexiones de datos administrados.
    
Para habilitar estos administradores de colección de sitios para el uso de soluciones de espacio aislado en Microsoft SharePoint Server 2010 o un servidor que ejecute Microsoft SharePoint Foundation 2010, el administrador de la granja debe iniciar el servicio de código del usuario de Windows SharePoint.
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a>Para iniciar el servicio de código del usuario de Windows SharePoint

1. Abra Administración central.
    
2. En **Servicios del sistema**, haga clic en **Administrar servicios en el servidor**.
    
3. Inicie el **Servicio de código del usuario de Microsoft SharePoint Foundation**.
    
### <a name="to-publish-a-sandboxed-solution"></a>Para publicar una solución de espacio aislado

1. Abra la plantilla de formulario en el diseñador de InfoPath.
    
2. Haga clic en la pestaña **Archivo** y, a continuación, haga clic en **SharePoint Server** en la ficha **Publicar** en Backstage. 
    
3. Escriba la dirección URL del sitio de SharePoint donde se realizará la publicación y haga clic en **Siguiente**. 
    
    > [!IMPORTANT]
    > [!IMPORTANTE] Debe ser administrador de una colección de sitios en este sitio para publicar esta plantilla de formulario como un solución de espacio aislado. 
  
4. Seleccione **Biblioteca de formularios** y, a continuación, haga clic en **Siguiente**.
    
5. Seleccione **Crear una nueva biblioteca de formularios** y, a continuación, haga clic en **Siguiente**.
    
6. Escriba el nombre y las descripciones de la biblioteca de formularios y, a continuación, haga clic en **Siguiente**.
    
7. Haga clic en **Publicar**.
    
Por ejemplo, soluciones que reflejan escenarios adecuados para plantillas de formularios publicadas como soluciones de espacio aislado, vea [Soluciones de espacio aislado de ejemplo](sample-sandboxed-solutions.md).
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a>Publicar plantillas de formularios como soluciones implementadas por el administrador

La publicación de formularios como plantilla aprobada por el administrador es una opción recomendada si el formulario tiene varias conexiones de datos, si requiere seguridad de plena confianza o si requiere una plantilla para toda la granja.
  
Existen varios pasos que un administrador de granja debe realizar para que la solución implementada por el administrador esté disponible en SharePoint; y como programador, se debe preparar la solución antes de que participe el administrador.
  
En primer lugar, si el formulario se va a implementar como de plena confianza, debe definir el nivel de seguridad tal como se describe en el procedimiento siguiente.
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a>Para definir el nivel de seguridad de una plantilla de formulario en plena confianza

1. Abra la plantilla de formulario en el diseñador de InfoPath.
    
2. Haga clic en la pestaña **Archivo**, en la ficha **Información** haga clic en **Opciones de formulario**.
    
3. Haga clic en la categoría **Seguridad y confianza** y después desactive la casilla **Determinar automáticamente el nivel de seguridad**. 
    
4. Seleccione **Plena confianza**.
    
A continuación, publique el formulario mediante el siguiente procedimiento, pero tenga en cuenta que existen algunas diferencias con un procedimiento de publicación estándar.
  
### <a name="to-publish-an-administrator-deployed-solution"></a>Para publicar una solución implementada por el administrador

1. En la primera página del **Asistente para publicación**, especifique la ubicación del sitio de SharePoint Server 2010 o SharePoint Foundation 2010 y haga clic en **Siguiente**.
    
2. InfoPath seleccionará automáticamente la casilla **Plantilla de formulario aprobada por el administrador** en la segunda página del asistente. Haga clic en **Siguiente**.
    
3. La tercera página es única para escenarios de implementación del administrador. En lugar de seleccionar un SharePoint Server, publique el formulario en un almacén local. El administrador de SharePoint cargará el archivo desde esta ubicación durante el proceso de implementación del administrador.
    
4. Complete las páginas restantes del **Asistente para publicación**.
    

