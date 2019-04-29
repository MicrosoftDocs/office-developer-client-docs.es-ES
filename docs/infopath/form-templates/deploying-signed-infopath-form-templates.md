---
title: Implementar plantillas de formulario de InfoPath firmadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8345a4bc-ad7b-d0b0-7615-f77ade35006d
description: Antes de leer este tema, vea la secciónPlantillas de formulario firmadasen Conceptos de seguridad adicionales de los formularios de InfoPath para comprender la seguridad de las plantillas de formulario firmadas. La información y los comentarios incluidos en el tema Niveles de seguridad, implementación en correo electrónico y plantillas de formulario remotas también son pertinentes.
ms.openlocfilehash: 76cc6dfdbd2c01827182c348281a98ad7cd17b69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426803"
---
# <a name="deploying-signed-infopath-form-templates"></a>Implementar plantillas de formulario de InfoPath firmadas

Antes de leer este tema, vea la sección "Plantillas de formulario firmadas" en [Conceptos de seguridad adicionales de los formularios de InfoPath](additional-infopath-form-security-concepts.md) para comprender la seguridad de las plantillas de formulario firmadas. La información y los comentarios incluidos en el tema [Niveles de seguridad, implementación en correo electrónico y plantillas de formulario remotas](security-levels-email-deployment-and-remote-form-templates.md) también son pertinentes. 
  
## <a name="digitally-signing-a-form-template"></a>Firmar digitalmente plantillas de formulario

Si firma digitalmente una plantilla de formulario, puede establecer el nivel de seguridad de la plantilla de formulario en plena confianza, lo que significa que el formulario puede tener acceso a los archivos y la configuración en el equipo del usuario o en un dominio diferente. (Además, la firma digital de una plantilla de formulario no impide usar otros niveles de seguridad, si lo prefiere. El nivel de seguridad de una plantilla de formulario firmada se establece en el nivel de seguridad de dominio o restringido.) Además, puede implementar la plantilla de formulario firmada para los usuarios que usen un programa de correo electrónico y, posteriormente, actualizar la plantilla de formulario firmada de forma automática enviando la versión actualizada a los usuarios como datos adjuntos de un mensaje de correo electrónico, siga estos pasos:
  
### <a name="to-digitally-sign-a-form-template"></a>Para firmar digitalmente plantillas de formulario

1. En InfoPath Designer, haga clic en la ficha **Archivo** y, a continuación, haga clic en **Opciones de formulario** en la ficha **Información**. 
    
2. En el cuadro de diálogo **Opciones de formulario**, haga clic en la categoría **Seguridad y confianza**. 
    
3. En **Firma de plantillas de formulario**, active la casilla **Firmar esta plantilla de formulario**. 
    
4. Haga clic en **Seleccionar certificado**.
    
5. En el cuadro de diálogo **Seleccionar certificado**, haga clic en el que desea usar para firmar digitalmente el formulario. 
    
> [!NOTE]
> [!NOTA] El botón **Crear certificado** del cuadro de diálogo **Opciones de formulario** se puede usar para generar un certificado de prueba con el que firmar una plantilla. El certificado de prueba debería usarse para firmar plantillas de formulario con fines de prueba únicamente. Los certificados de prueba no deben usarse para firmar plantillas de formulario que se vayan a distribuir públicamente. Como los certificados no están emitidos por una entidad de certificación cuyo certificado raíz ya es de confianza en el equipo de un usuario, el certificado de prueba no se validará correctamente en el equipo del usuario. Si implementa una plantilla de formulario firmada con un certificado de prueba, es probable que los usuarios no puedan abrirla. 
  
## <a name="establishing-a-trusted-root-certificate-and-publisher"></a>Establecer un publicador y un certificado raíz de confianza

 El certificado raíz de confianza que se usa para firmar la plantilla de formulario debe estar en el almacén de certificados raíz de confianza del equipo del usuario. De lo contrario, no se podrá comprobar el publicador de la plantilla de formulario y los usuarios de la misma no tendrán la opción de confiar en el publicador. Si el certificado raíz de confianza está en el almacén de certificados raíz de confianza, pero el publicador no está en la lista de publicadores de confianza, se ofrece a los usuarios la opción de confiar en el publicador de la plantilla. 
  
> [!NOTE]
> [!NOTA] Si una plantilla de formulario firmada solicita acceso Restringido o Dominio, InfoPath usará la firma para comprobar que la plantilla de formulario no se manipuló después de haberse firmado. InfoPath también usa la firma para determinar si la plantilla puede actualizarse automáticamente. 
  
## <a name="deploying-signed-form-templates-with-full-trust-access"></a>Implementar plantillas de formulario firmadas con acceso de plena confianza

El primer paso para implementar plantillas de formulario firmadas consiste en habilitar la funcionalidad como dominio, como la actualización automática, en formularios de plena confianza. Una plantilla de formulario firmada que solicita acceso de plena confianza tiene el mismo acceso a los recursos del sistema que un  *formulario de plena confianza*  . Para obtener información detallada sobre cómo funcionan los formularios de plena confianza y cómo crearlos e implementarlos, vea [Descripción de los formularios de plena confianza](understanding-fully-trusted-forms.md).
  
Sin embargo, según el entorno informático de la organización, tal vez prefiera usar plantillas de formulario firmadas o formularios de plena confianza. Por ejemplo, existen ventajas si se usa una plantilla de formulario firmada que solicita acceso de plena confianza, en lugar de un formulario de plena confianza registrado. Una plantilla de formulario firmada que solicita acceso de plena confianza presenta las ventajas siguientes:
  
- No es preciso registrarla, a diferencia de las plantillas de formulario de plena confianza no firmadas.
    
- Permite su actualización automática silenciosa.
    
Como no es preciso registrar una plantilla de formulario firmada que solicita acceso de plena confianza, no es necesario usar un paquete de instalador ni un archivo de script para implementarla. Esta ventaja simplifica mucho la implementación de las plantillas de formulario de plena confianza.
  
Cuando actualice la plantilla de formulario firmada que solicita acceso de plena confianza, puede sencillamente enviar la plantilla actualizada al usuario o actualizarla en una ubicación compartida. Cuando el usuario abra la plantilla actualizada, no se le pedirá confirmación y la versión actualizada sobrescribirá de forma silenciosa la copia anterior existente en el equipo. Si actualiza la plantilla en una ubicación compartida, el usuario podrá usar la copia actualizada sin que se le pida confirmación.
  
Si desea actualizar un formulario de plena confianza no firmado, deberá empaquetarlo y registrarlo de nuevo. Además, una plantilla de formulario de plena confianza instalada funciona solo para la ruta del equipo local, pero no funciona en una ruta de acceso de red, porque el proceso de registro no admite cambiar una ruta de acceso de equipo local por una ruta de acceso de red. Sin embargo, como es necesario un certificado para firmar una plantilla de formulario, tal vez prefiera implementar plantillas de formulario de plena confianza registradas para no tener que adquirir un certificado.
  
## <a name="deploying-signed-form-templates-with-domain-or-restricted-access"></a>Implementar plantillas de formulario firmadas con acceso Restringido o Dominio

Una plantilla de formulario firmada que tiene un nivel de seguridad Restringido o Dominio también presenta la ventaja de disponer de la funcionalidad de actualización automática. Por ejemplo, podría publicar una plantilla de formulario firmada en una biblioteca de documentos en un servidor en el que se ejecute Microsoft SharePoint Foundation o en un servidor con un nivel de seguridad Dominio. Cuando actualice la plantilla de formulario en la ubicación compartida, los usuarios recibirán la copia actualizada automáticamente.
  

