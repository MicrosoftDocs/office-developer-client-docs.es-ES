---
title: Niveles de seguridad, implementación de correo electrónico y plantillas de formulario remotas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fc438ad-ae26-3632-3444-371537eaecb3
description: Microsoft InfoPath admite mover plantillas de formulario de una ubicación a otra, enviarlas como datos adjuntos a un mensaje de correo electrónico y crear plantillas de formulario de plena confianza que estén firmadas digitalmente o instaladas.
ms.openlocfilehash: 799f2b19bfc4daa4a177d789a811d20ca09e7153
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396879"
---
# <a name="security-levels-email-deployment-and-remote-form-templates"></a>Niveles de seguridad, implementación de correo electrónico y plantillas de formulario remotas

Microsoft InfoPath admite mover plantillas de formulario de una ubicación a otra, enviarlas como datos adjuntos a un mensaje de correo electrónico y crear plantillas de formulario de plena confianza que estén firmadas digitalmente o instaladas.
  
## <a name="security-levels"></a>Niveles de seguridad

Las plantillas de formulario pueden tener uno de los tres niveles de seguridad existentes, en función de donde se encuentren ubicadas. Estos tres niveles de seguridad se describen en las secciones siguientes. 
  
### <a name="restricted"></a>Restringido

El nivel de seguridad Restringido no permite ninguna comunicación fuera de la plantilla de formulario. Este nivel de seguridad está concebido para impedir que los formularios dañinos transmitan datos desde su PC a un atacante malintencionado. Cuando se use este modo de seguridad, las características siguientes no funcionarán:
  
- Paneles de tareas HTML  
- Consulta de SharePoint
- Envío de SharePoint
- Consulta de archivos XML
- Consulta de bases de datos
- Envío de bases de datos
- Consulta de servicios web
- Envío de servicios web
- Envío de código personalizado
- Envío al entorno de hospedaje
- Controles ActiveX
- Roles
- Flujo de trabajo de SharePoint
- Reglas que abren un nuevo documento
- Código administrado
- Vista de impresión externa
- Imágenes vinculadas
    
### <a name="domain"></a>Dominio

El nivel de seguridad Dominio restringe un formulario a un dominio de Internet concreto y los permisos están limitados a la configuración de Internet Explorer para la zona donde se encuentre el dominio. El formulario puede comunicarse con orígenes de datos contenidos en el mismo dominio pero, por lo general, no podrá recuperar datos de otros dominios salvo que la zona permita la comunicación entre dominios. Se trata del nivel de seguridad mínimo para las plantillas de formulario compatibles con explorador.
  
### <a name="full-trust"></a>Plena confianza

El nivel de seguridad Plena confianza permite ejecutar un formulario de plena confianza en el equipo en el que se va a usar. Este nivel de seguridad únicamente se puede usar cuando se trabaja con un formulario que se encuentra en un servidor firmado con una firma que coincide con un publicador raíz de confianza del equipo o instalando el formulario. Ambos métodos requieren establecer el atributo **requireFullTrust** en "sí". Con esta configuración, el formulario tiene acceso a llamadas al modelo de objetos, como guardar archivo, y a algunas solicitudes de seguridad que aparecen cuando se ejecuta en un nivel de seguridad más restringido están deshabilitadas. 
  
> [!NOTE]
> [!NOTA] Todos los formularios generados en InfoPath Designer tienen un nivel de seguridad asociado. InfoPath abre los formularios en su nivel de seguridad asociado, pero si este nivel es superior al nivel que se le puede conceder, el formulario no se abrirá. 
  
El nivel de seguridad Plena confianza sólo se puede establecer para las plantillas de formulario instaladas o firmadas; en caso contrario, el nivel máximo de confianza es Dominio. InfoPath no establecerá automáticamente un nivel de seguridad en plena confianza.
  
A los formularios se les conceden niveles de seguridad en función de la ubicación desde la que se abren.
  
## <a name="trust-levels"></a>Niveles de confianza

El nivel más elevado de confianza que se puede conceder a una plantilla de formulario lo determina la ubicación desde donde se abre y otro código de comprobación, como se describe en la tabla siguiente. Los atributos que aparecen en la tabla (por ejemplo, HTTP, UNC, *requireFullTrust*) son entradas que se utilizan para determinar el nivel de confianza que se puede conceder a un formulario y se aplica a formularios abiertos en el cliente de InfoPath. 
  
|Nivel de confianza más elevado concedido|Plena confianza|Equipo cliente (espacio aislado)|Intranet (espacio aislado)|Internet (espacio aislado)|Restringido|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|
|**archivo: ruta de acceso=ubicación desde donde se abre** <br/> |||X  <br/> |||
|**archivo: ruta de acceso\<\>abiertos desde la ubicación o sin ruta de acceso (independientemente de donde la procedencia del formulario)** <br/> |||||X  <br/> |
|**Ubicación desde donde se abre: Intranet HTTP o HTTPS** <br/> |||X  <br/> |||
|**Ubicación desde donde se abre: Internet HTTP o HTTPS** <br/> ||||X  <br/> ||
|**Ubicación desde donde se abre: UNC** <br/> |||X  <br/> |||
|**Plantilla instalada (requireFullTrust="sí")** <br/> |X  <br/> |||||
|**Plantilla instalada (requireFullTrust="no")** <br/> ||X  <br/> ||||
|**Plantilla con certificado de publicador de confianza** <br/> |X  <br/> |||||
|**Archivos de formulario exportados** <br/> |||X  <br/> |||
   
## <a name="form-open-behavior"></a>Comportamiento de apertura del formulario

Todos los archivos que se abren en InfoPath Editor están sujetos a un conjunto de condiciones que determinan el nivel de seguridad con el que se abrirá el formulario, así como si se abrirá o no. Cuando se abre un formulario en InfoPath Editor, tiene que abrirse con el nivel de seguridad adecuado o, de lo contrario, no se cargará. Si un formulario solicita un nivel de seguridad superior al que se le puede conceder (un formulario puede solicitar un nivel de seguridad concreto mediante los atributos **trustLevel** o **requireFullTrust**), no se podrá cargar; si no, se cargará con el nivel de seguridad que solicita. Si no se permite abrir la plantilla de formulario con el nivel de seguridad solicitado, el usuario no podrá abrir el formulario y recibirá un mensaje de error. 
  
En la tabla siguiente se describen las condiciones necesarias para abrir un formulario con los distintos niveles de seguridad y el comportamiento resultante cuando los usuarios intentan abrirlo.
  
|El editor se abre/da error|Plena confianza (requireFullTrust="sí")|Confianza del dominio (trustLevel="Dominio" o en blanco)|Restringido (trustLevel="Restringido")|
|:-----|:-----|:-----|:-----|
|**De confianza (certificado de confianza o instalado)** <br/> |El editor se abre en el nivel de plena confianza  <br/> |N/D  <br/> |N/D  <br/> |
|**Confianza del dominio: Equipo cliente** <br/> |Error al abrir  <br/> |El editor se abre en el nivel de dominio  <br/> |El editor se abre en el nivel Restringido  <br/> |
|**Confianza del dominio: Intranet** <br/> |Error al abrir  <br/> |El editor se abre en el nivel de dominio  <br/> |El editor se abre en el nivel Restringido  <br/> |
|**Confianza del dominio: Internet** <br/> |Error al abrir  <br/> |El editor se abre en el nivel de dominio  <br/> |El editor se abre en el nivel Restringido  <br/> |
|**Restringido** <br/> |Error al abrir  <br/> |Error al abrir  <br/> |El editor se abre en el nivel Restringido  <br/> |
   
## <a name="specifying-a-security-level"></a>Especificación de un nivel de seguridad

El diseñador de formularios de InfoPath selecciona automáticamente el nivel de seguridad adecuado (Restringido o Dominio) basándose en las características que se están usando en el formulario. La configuración de seguridad siempre es lo más restrictiva posible, empezando por Restringido, para ayudar a garantizar un nivel de protección superior para el usuario y sus datos. Los usuarios pueden anular manualmente esta configuración automática y seleccionar otro nivel de seguridad más adecuado para el formulario siguiendo estos pasos:
  
1. Haga clic en la ficha **Archivo** y, a continuación, en **Opciones de formulario** en la ficha **Información**. 
    
2. En la lista **Categorías**, haga clic en **Seguridad y confianza**.
    
3. Desactive la casilla **Determinar automáticamente el nivel de seguridad (recomendado)**. 
    
4. Seleccione el nivel de seguridad deseado.
    
## <a name="mail-deployment-and-browser-enabled-form-templates"></a>Implementación de correo y las plantillas de formulario habilitadas para explorador

InfoPath permite enviar las plantillas de formulario como datos adjuntos a un mensaje de correo electrónico y mover de una ubicación a otra. La implementación en el correo es un modo sencillo y eficaz de distribuir formularios para su uso dentro de la organización y también para implementar formularios para usuarios remotos.
  
De forma alternativa, si dispone de Microsoft SharePoint Server 2010 con InfoPath Forms Services, puede crear plantillas de formulario que permiten a los usuarios que no tienen InfoPath instalado rellenar formularios en un explorador web.
  
## <a name="understanding-form-identity"></a>Descripción de la identidad de los formularios

Todos los formularios de InfoPath Designer se crean con una identidad. La información de esta identidad sirve para que InfoPath asocie formularios con plantillas de formulario en la memoria caché y para recuperar las actualizaciones de los formularios cuando se envían a una ubicación compartida. De manera predeterminada, InfoPath crea dos identidades para las plantillas de formulario: un id. de formulario y una ruta de acceso. 
  
### <a name="form-id"></a>Id. de formulario

Se trata de un identificador único basado en un prefijo, el nombre del formulario y su espacio de nombres. El identificador debe ser un nombre único que se puede usar para asociar correctamente los archivos de formulario con su plantilla de formulario asociada en la memoria caché del equipo cliente. El id. de formulario se especifica como el atributo de nombre (por ejemplo,  `name="urn:MyForm:MyCompany:Template1:myXSD-1583-78-G3V94-23-47"`) en el archivo de definición del formulario (.xsf). 
  
### <a name="access-path"></a>Ruta de acceso

Se trata de un identificador de ubicación que se usa para determinar la ubicación correcta de la plantilla de formulario, así como la ubicación para recibir actualizaciones. Cuando se guarda o se publica, el lugar en el que se guarda o publica la plantilla de formulario pasa a ser la ruta de acceso predeterminada. Cada vez que un formulario se abre en el equipo cliente, intenta asociarse a un formulario almacenado en memoria caché. Al hacerlo, seguirá el orden siguiente:
  
1. Busca una plantilla de formulario de plena confianza con un id. de formulario coincidente.
    
2. Busca una plantilla de formulario en la memoria caché con una ruta de acceso coincidente.
    
3. Busca una plantilla de formulario en la memoria caché con un id. de formulario coincidente.
    
Una vez encontrada la coincidencia, el formulario se abrirá con la plantilla asociada. En los casos en los que se estableció la coincidencia con una ruta de acceso, InfoPath la usará para recuperar actualizaciones para la plantilla de formulario. Este método simplifica la administración, el mantenimiento y la actualización de formularios en la organización. Si no se puede establecer la coincidencia y el nivel de confianza es Dominio, el formulario no se abrirá. La ruta de acceso se especifica como el atributo **publishUrl** en el archivo de definición del formulario (.xsf). 
  
Al igual que existen dos propiedades de identificación por cada plantilla de formulario, hay una heurística para determinar específicamente las entradas resultantes en la memoria caché, según la condición de la plantilla de formulario (bien sea la ruta de acceso, el id. del formulario o ambos) y el estado de la conexión de red.
  
## <a name="designing-a-form-to-send-as-an-attachment-to-an-email-message"></a>Diseñar un formulario para enviarlo como datos adjuntos a un mensaje de correo electrónico

Todos los formularios que se crean en el Diseñador de InfoPath se pueden enviar a los usuarios como datos adjuntos a un mensaje de correo electrónico. Implementación de correo electrónico es una forma sencilla y eficaz para distribuir formularios para su uso entre oficinas y también para implementar formularios a los usuarios remotos.
  
### <a name="to-mail-a-form-template-to-other-users"></a>Para enviar por correo una plantilla de formulario a otros usuarios

1. Haga clic en la pestaña **archivo** , haga clic en **Publicar**y, a continuación, haga clic en el botón **correo electrónico** . 
    
2. Rellene las dos páginas siguientes del **Asistente para publicación** y haga clic en **Siguiente** para pasar por todas las páginas y, por último, haga clic en **Publicar**.
    
3. Se muestra un mensaje de correo electrónico que permite rellenar la lista de destinatarios y las instrucciones adicionales que es posible que deba para ellos.
    
4. Una vez terminado, haga clic en **Enviar**. El formulario y la plantilla de formulario se adjuntarán al mensaje.
    
## <a name="email-deployment-restricted-domain-and-full-trust-form-templates"></a>Implementación de correo electrónico: restringido, dominio y las plantillas de formulario de plena confianza

Implementación de correo electrónico de plantillas de formulario con nivel restringido permite que los formularios dinámicos sin conexiones de datos que se abrirá desde cualquier lugar. Los destinatarios pueden abrir plantillas de formulario enviadas como datos adjuntos de correo electrónico directamente desde Microsoft Outlook 2010 o desde cualquier lugar en que el destinatario haya guardado los datos adjuntos. Asimismo, Outlook 2010 permite a los usuarios editar los formularios directamente en el mensaje.
  
Plantillas de formulario con el nivel de confianza de dominio se deben abrir desde su ubicación publicada, pero mediante la publicación a una lista de destinatarios de correo electrónico en el Asistente para publicación, se pueden enviar como datos adjuntos a un mensaje de correo electrónico. Cuando se abren los datos adjuntos, funcionan como un vínculo con la ubicación real de publicación de la plantilla. La plantilla de formulario de esta ubicación es lo que realmente se abre en InfoPath Editor.
  
Uso de una plantilla de formulario de nivel de dominio enviada como datos adjuntos de correo electrónico es similar a con cualquier otro tipo de documento; Por ejemplo, un libro de Microsoft Excel o un documento de Microsoft Word. Un usuario sólo tiene que hacer clic en el formulario para abrirlo y usarlo. Además, los usuarios tienen a su disposición todas las ventajas de las actualizaciones del nivel Dominio.
  
Puede enviar por correo electrónico de las plantillas de formulario que soliciten acceso de plena confianza, pero estas plantillas deben estar firmadas o no se permitirá a abrir. Las plantillas de formulario que solicita acceso restringido o dominio no es necesario iniciar sesión para que se envíen como datos adjuntos de correo electrónico. InfoPath no comprueba la firma, ni siquiera cuando la plantilla está firmada, excepto para ver si puede actualizarse automáticamente. Es posible firmar digitalmente una plantilla de formulario de nivel Restringido o Dominio y seguir manteniendo la capacidad de actualización automática. En este caso, la firma digital evitará que se muestren mensajes de conflicto de memoria caché.
  
## <a name="sharing-forms-by-email-message-or-from-a-common-shared-location"></a>Compartir formularios por mensaje de correo electrónico o desde una ubicación compartida común

Algunas preguntas que deben considerarse al crear un formulario que será implementado por mensaje de correo electrónico.
  
- **¿Se actualizará el formulario con regularidad?** Si está creando un formulario que se va a actualizar con regularidad, debería publicarlo en una ubicación compartida antes de enviarlo a los usuarios. De este modo, podrá actualizarlo publicando nuevas versiones en la ubicación compartida, pero también podrá distribuir la plantilla de formulario de forma inmediata a los usuarios que tal vez no tengan acceso a la ubicación compartida. 
    
   Si un formulario se actualiza y, a continuación, se distribuyen por mensaje de correo electrónico, los usuarios recibirán un mensaje de conflicto de la memoria caché cuando intenten abrir el nuevo formulario, si tienen una versión anterior almacenada en su equipo y la ruta de acceso ha cambiado. Se le pedirá al usuario que elija la versión que desea usar. Incluso si el formulario actualizado es el mismo que el que tiene en su equipo, el usuario recibirá un mensaje de conflicto de memoria caché y se le pedirá que elija la copia que va a usar. La práctica recomendada en esta situación es compartir el formulario desde una ubicación compartida.
    
- **¿Tiene acceso el formulario a una conexión de datos o usa otras características no admitidas en el nivel de seguridad Restringido?** Si está desarrollando un formulario que exige seguridad de nivel Dominio, InfoPath requiere que se publique el formulario en una ubicación compartida para que los usuarios puedan abrirlo. Debido a que las plantillas de formulario sólo se abrirán en el nivel de seguridad que se solicitan, formularios abiertos directamente desde un mensaje de correo electrónico no se abrirán si InfoPath no puede conceder la seguridad de nivel de dominio. 
    
## <a name="benefits-of-using-signed-form-templates"></a>Ventajas del uso de plantillas de formulario firmadas

- Permite abrir la plantilla de formulario con el nivel de seguridad Plena confianza.
    
- Evita los mensajes de conflicto de la memoria caché si se mueve el formulario a una nueva ubicación.
    
Asimismo, si una plantilla de formulario está firmada, disfrutará de la ventaja adicional de la funcionalidad de actualización automática. Para obtener más información, vea [Implementar plantillas de formulario de InfoPath firmadas](deploying-signed-infopath-form-templates.md).
  
### <a name="example-updating-domain-or-restricted-templates"></a>Ejemplo: Actualizar plantillas restringidas o dominio

En el ejemplo siguiente se muestra cómo una plantilla de formulario firmada y actualizada que solicita acceso restringido o dominio puede sobrescribir una copia anterior: 
  
1. "A" envía una plantilla de formulario firmada a "B".
    
2. "B" abre la plantilla de formulario.
    
3. "A" actualiza la plantilla de formulario (por ejemplo, agrega más campos).
    
4. "A" envía la plantilla de formulario actualizada a "B".
    
5. "B" abre la plantilla de formulario actualizada.
    
### <a name="example-deploying-restricted-form-templates-on-an-extranet"></a>Ejemplo: Implementar restringidos plantillas de formulario en una extranet
  
1. Guarde la plantilla de formulario de dominio en un sitio Web que ejecuta Microsoft SharePoint Foundation 2010.
    
2. Cambie el nivel de seguridad de la plantilla de formulario a Restringido.
    
3. Guarde la plantilla de formulario en el escritorio de su equipo.
    
4. Quite la dirección URL (solo si los usuarios tienen acceso a la ubicación de publicación original).
    
5. Envíe el formulario a los usuarios de la extranet.
    
6. Pida a los usuarios que lo instalen.
    
7. Pida a los usuarios que se lo devuelvan después de haberlo rellenado.
    
8. Guardar el formulario en el sitio Web que ejecuta SharePoint Foundation 2010 y vuelva a vincular el formulario utilizando la opción **volver a vincular documentos a esta biblioteca** en la página **Configuración de biblioteca de formularios** . 
    
## <a name="signature-verification-failure"></a>Error de comprobación de firma

Una plantilla de formulario firmada que solicita acceso de plena confianza pero cuya firma no se puede autenticar no se abrirá. La comprobación de la firma puede dar error por alguna de las razones siguientes:
  
- El certificado raíz no está en el almacén de certificados raíz de confianza.
    
- El certificado que se usó para firmar la plantilla de formulario ha caducado.
    
- El certificado usado para firmar la plantilla de formulario ha sido revocado.
    
- La firma de la plantilla de formulario está dañada (lo que indica que la plantilla se modificó después de haberse firmado).
    
Si una plantilla de formulario firmada solicita acceso Restringido o Dominio, InfoPath no comprobará la firma salvo para determinar si puede actualizarse automáticamente.
  
## <a name="infrastructure-registry-keys-for-form-migration-open-behavior"></a>Comportamiento de apertura de las claves del registro de infraestructura para la migración de formulario

Cuando un usuario intenta abrir un formulario que coincide con una plantilla de formulario en el id. de formulario, InfoPath mostrará un mensaje de error si la plantilla de formulario tiene un nivel de confianza Dominio y el dominio no coincide con el atributo  *href*  del formulario. Esto evita que se abran formularios que no se crearon explícitamente con la plantilla de formulario. 
  
InfoPath no permite que coexistan plantillas de formulario con el mismo id. de formulario. Hay cuatro claves del Registro adicionales que ayudan a los administradores del sistema a dar la opción a los usuarios de permitir abrir el archivo XML con una plantilla de formulario. Este modelo también permite a los administradores definir el comportamiento de apertura que desean para los formularios.
  
En la tabla siguiente se describe la configuración predeterminada de las claves del Registro. Si estas claves no están presentes, se aplicará el valor predeterminado especificado en la tabla.
  
Los valores Nombre corresponden a la configuración de dominio de Internet Explorer. Estos valores determinan el comportamiento de apertura del formulario en estas zonas de seguridad, ya sea bloqueando o permitiendo la apertura del formulario, o dando al usuario la opción de abrirlo.
  
|**Valor Nombre**|**Bloquear**|**Interfaz de usuario**|**Permitir**|
|:-----|:-----|:-----|:-----|
|**Internet** <br/> |X  <br/> |||
|**Intranet** <br/> ||X  <br/> ||
|**Equipo cliente** <br/> |||X  <br/> |
|**Sitio de confianza** <br/> |||X  <br/> |
   
Es la ruta de la clave del registro `HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\InfoPath\Open Behaviors`.

El comportamiento de apertura del formulario se define como sigue:
  
- `Block [REG_DWORD = 0]`- Se muestra un cuadro de diálogo de error con un botón Ayuda. InfoPath no permitirá que el archivo XML se abra cuando el formulario se ejecute en la zona de seguridad especificada y no coincida con el dominio de la plantilla. 
    
- `User Interface [REG_DWORD = 1]`- Se muestra el cuadro de diálogo Sí/No. InfoPath pedirá al usuario que abra el archivo XML con la plantilla de formulario cuando el formulario se ejecute en la zona de seguridad especificada y no coincida con el dominio de la plantilla. 
    
- `Allow [REG_DWORD = 2]`- El archivo XML se abrirá sin cuadros de diálogo de advertencia o error. InfoPath permitirá que se abra el archivo XML cuando el formulario se ejecute en la zona de seguridad especificada y no coincida con el dominio de la plantilla. 
    
Si se abre un formulario con una plantilla de formulario que se ejecuta en el nivel de seguridad Dominio y el dominio de seguridad de la ubicación "en memoria caché" de la plantilla (es decir, donde el formulario se guarda en memoria caché) y el atributo **href** del formulario no coinciden, InfoPath comprobará el Registro para definir el comportamiento de apertura del formulario. El comportamiento permitido se basará en la zona de seguridad en la que se encuentre la plantilla (el valor  *CachedFromLocation*  ). 
  
Por ejemplo, cuando un formulario coincide con una plantilla de formulario en el id. de formulario pero no en la ruta de acceso y la plantilla está almacenada en memoria caché en una ubicación de Internet, InfoPath mostrará un cuadro de diálogo de error con un botón Ayuda.
  
> [!NOTE]
> [!NOTA] Los formularios de InfoPath no se abrirán cuando el dominio sea un dominio restringido de Internet Explorer, por tanto, no hay clave del Registro para los sitios restringidos de Internet Explorer. 
  

