---
title: Solución de problemas de los archivos de Office y soluciones personalizadas con el registro de telemetría
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: ef88e30e-7537-488e-bc72-8da29810f7aa
description: Use Registro de telemetría de Office 2013 para determinar problemas de compatibilidad con Office 2013 y soluciones generadas para las versiones anteriores de Office.
localization_priority: Priority
ms.openlocfilehash: 3954662a9476dca0cbb9bf4b8197979783b7e11e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715168"
---
# <a name="troubleshooting-office-files-and-custom-solutions-with-the-telemetry-log"></a>Solución de problemas de los archivos de Office y soluciones personalizadas con el registro de telemetría

Use Registro de telemetría de Office 2013 para determinar problemas de compatibilidad con Office 2013 y soluciones generadas para las versiones anteriores de Office.
  
En el siguiente artículo se describe el Registro de telemetría y cómo usarlo. Para obtener más información sobre los resultados específicos que se muestran en Registro de telemetría, vea [Problemas de compatibilidad en Office](compatibility-issues-in-office.md).

En numerosas versiones anteriores, Microsoft proporcionó herramientas y marcos para personalizar, automatizar y extender Office. Esto permitió a empresas y usuarios generar soluciones o complementos para que las aplicaciones de Office resulten más productivas y eficaces. La complejidad de estas soluciones oscila desde macros sencillas de Visual Basic para Aplicaciones (VBA) hasta sólidas personalizaciones de .NET Framework. Muchos usuarios que disponen de estas soluciones confían en ellas para completar tareas esenciales para sus empresas, y es posible que ni siquiera sean conscientes de que están usando una personalización agregada a las aplicaciones de Office.
  
Con semejante proliferación de soluciones de Office, la actualización de versiones de Office puede resultar compleja. Las empresas y los usuarios no saben si esas soluciones tan valiosas resultan plenamente compatibles con la nueva versión, ya que podrían usar características y código informático disponibles en versiones anteriores de Office que quedaron en desuso en las versiones posteriores. Si una solución que usa una característica desusada se carga en la aplicación host, es posible que se comporte de manera diferente, que provoque un error, que no se cargue o que cause el bloqueo de la aplicación host.
  
Registro de telemetría de Office 2013, una herramienta basada en Excel 2013, muestra eventos relacionados con la selección de aplicaciones de Office 2013 para ayudar a los desarrolladores y usuarios con experiencia a diagnosticar problemas de compatibilidad. Con esta herramienta, los usuarios pueden determinar los posibles problemas con relación a los complementos que usan en su entorno de trabajo, y proporcionar a los responsables de las decisiones empresariales la información necesaria para decidir si deben o no actualizarse a Office 2013. Asimismo, Registro de telemetría proporciona comentarios detallados sobre el proceso de desuso o los cambios específicos de los modelos de objetos de las aplicaciones de Office 2013, lo que permite a los desarrolladores identificar y refactorizar rápidamente el código o los controles problemáticos. Los profesionales de TI pueden ver las tendencias en el estado de las soluciones en varios clientes con el Panel de telemetría para Office 2013, una herramienta complementaria de Registro de telemetría.
  
Para obtener más información, vea [Implementar el Panel de telemetría de Office](https://technet.microsoft.com/library/f69cde72-689d-421f-99b8-c51676c77717).
  
## <a name="how-the-telemetry-log-works"></a>Funcionamiento de Registro de telemetría
<a name="OEV_Types"> </a>

Cuando se carga, usa, cierra un archivo o solución de Office o bien cuando este genera un error en una de las aplicaciones seleccionadas de Office 2013, la aplicación añade un registro en el almacén de datos local (una base de datos del mismo equipo) que incluye información sobre el evento. El registro incluye un título para el evento, la aplicación que registró el evento, la hora, el nombre del archivo o la solución, la gravedad y una breve descripción de los errores que se hubieran podido producir. Cuando se actualiza, el libro de Registro de telemetría muestra una lista de los registros contenidos en el almacén de datos local.
  
> [!NOTE]
> La ubicación predeterminada para el almacén de datos local es %Users%\[Current user]\AppData\Local\Microsoft\Office\15.0\Telemetry. El tamaño máximo predeterminado para el almacén de datos es de 5 MB (5.120 KB).. 
  
Las aplicaciones de Office 2013 seleccionadas tienen una API de registro de tiempo de ejecución que crea un registro en el almacén de datos local cada vez que un archivo o una solución genera uno de los siguientes eventos:
  
- **OnLoad**: se crea un registro en el almacén de datos local cuando se carga un archivo o una solución en las aplicaciones de Office 2013 específicas. Los registros de error en tiempo de ejecución incluyen el nombre de archivo, ubicación y otra información en el almacén de datos local cuando se genera un evento de **OnLoad**. 
    
- **OnClose**: se crea un registro cuando se cierra un archivo o solución dentro de la aplicación. El registro incluye el nombre de la solución o del archivo, su ubicación y la aplicación que registró el evento.
    
- **OnError**: se crea un registro cuando se encuentra un error en una solución para determinadas aplicaciones de Office 2013. El registro incluye el nombre de la solución o del archivo y el error en tiempo de ejecución o el problema de compatibilidad que encontró el usuario. En la medida de lo posible, los errores se asignan a problemas de compatibilidad conocidos y se muestran como tales en Registro de telemetría.
    
Registro de telemetría muestra información acerca de una gran lista de archivos y tipos de solución para una selección de aplicaciones de Office 2013. El tipo de archivos y soluciones que supervisan las API de registro en tiempo de ejecución varían de una aplicación a otra. Consulte la Tabla 1 para obtener más información acerca de los tipos de soluciones que se supervisan.
  
### <a name="table-1-types-of-office-files-and-solutions-tracked-in-telemetry-log"></a>Tabla 1. Tipos de archivos y soluciones de Office supervisados en Registro de telemetría
<a name="OEV_Table1"> </a>

|**Tipo de solución**|**Aplicaciones**|**Descripción**|
|:-----|:-----|:-----|
|Aplicaciones del panel de tareas  <br/> |Excel 2013, Word 2013, Project 2013  <br/> |Son Complementos de Office que se hospedan en un panel de tareas de la aplicación cliente.  <br/> |
|Aplicaciones de contenido  <br/> |Excel 2013  <br/> |Son Complementos de Office integradas en el contenido del archivo de Office.  <br/> |
|Aplicaciones de correo  <br/> |Outlook 2013  <br/> |Son aplicaciones que se muestran en Outlook 2013 cuando se cumplen ciertas condiciones (cuando el asunto o el cuerpo de un mensaje de correo incluyen ciertas palabras o frases).  <br/> |
|Documentos activos  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> | Los documentos activos son cualquier archivo de documento de Office distintos de los tipos de soluciones que aparecen en esta tabla. Esto puede incluir lo siguiente:  <br/>  Archivos de formato binario de Office (.doc, .ppt, .pps, .xls).  <br/>  Archivos de formato OpenXML de Office (.docx, .pptx, .ppsx, .xlsx).  <br/>  Archivos habilitados para macros que contienen código VBA (.docm, .dotm, .pptm, .potm, .xlsm, .xltm).  <br/>  Archivos que contienen controles ActiveX.  <br/>  Archivos que tienen conexiones de datos externos.  <br/> |
|Complementos COM  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> Outlook 2013  <br/> |Los complementos COM incluyen complementos de Herramientas de desarrollo de Office en Visual Studio 2010 en el nivel de aplicación.  <br/> |
|Complementos de automatización de Excel  <br/> |Excel 2013  <br/> |Este tipo de solución incluye versiones anteriores de complementos de automatización compatibles con Excel, que se crean en complementos COM. Las funciones de los complementos de automatización pueden llamarse desde las fórmulas en las hojas de cálculo de Excel.  <br/> |
|Complementos XLL de Excel  <br/> |Excel 2013  <br/> |Los complementos XLL (.xll) con específicos de Excel y se crean con cualquier compilador que admita la creación de archivos DLL (bibliotecas de vínculos dinámicos). No es necesario que estén instalados ni registrados. Los complementos XLL también incluyen archivos DLL que contienen comandos y funciones definidos por el usuario.  <br/> |
|Complementos XLS RTD de Excel  <br/> |Excel 2013  <br/> |Los complementos de datos en tiempo real (RTD) XLS son hojas de cálculo de Excel que usan la función de hoja de cálculo de **RealTimeData** para llamar a un servidor de automatización y recuperar datos en tiempo real.  <br/> |
|Complementos WLL de Word  <br/> |Word 2013  <br/> |Los complementos WLL (.wll) son específicos de Word y se crean con cualquier compilador compatible que permita compilar DLL.  <br/> |
|Complementos de aplicaciones  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> |Los complementos de aplicaciones son archivos específicos de las aplicaciones que contienen código VBA. Incluyen los complementos de PowerPoint (.ppa, .ppam) y Excel (.xla, .xlam), y las plantillas de Word habilitadas para macros (.dotm).  <br/> |
|Plantillas  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> |Las plantillas incluyen plantillas de documentos (.dot, .dotx), de hojas de cálculo (.xlt, .xltx) o de presentaciones (.pot, .potx) que están vinculadas a un archivo de Office.  <br/> |
   
## <a name="using-the-office-telemetry-log"></a>Usar el registro de telemetría de Office
<a name="OEV_Using"> </a>

Al instalar Office 2013, se instala Registro de telemetría, se crea el almacén de datos local en el mismo equipo y se habilitan las API de registro en tiempo de ejecución en las aplicaciones de Office 2013 indicadas anteriormente. Sin embargo, debe cargarse o abrirse una solución o archivo en la aplicación para que Registro de telemetría pueda comenzar a supervisarla.
  
Use el siguiente procedimiento para mostrar los problemas registrados de Office en Registro de telemetría. 
  
### <a name="to-use-the-telemetry-log"></a>Procedimiento para usar Registro de telemetría

1. Para abrir Registro de telemetría, realice uno de los procedimientos siguientes:
    
   - **En Windows 7:** en el menú **Inicio**, elija **Todos los programas** y, en la lista de programas, expanda **Microsoft Office 2013** y **Herramientas de Office 2013**. A continuación, haga clic en **Registro de telemetría de Office 2013**.
    
     Se abrirá un libro nuevo en Excel 2013. El libro nuevo tiene tres hojas de cálculo con los títulos **Eventos**, **Info. del sistema** y **Guía**.
    
   - **En Windows 8:** deslice hacia arriba para mostrar la barra de aplicaciones, elija **Todas las aplicaciones** y seleccione **Registro de telemetría de Office 2013**.
    
     Se abrirá un libro nuevo en Excel 2013. El libro nuevo tiene tres hojas de cálculo con los títulos **Eventos**, **Info. del sistema** y **Guía**.
    
2. Para ver una lista actualizada de eventos, en la parte superior de la hoja de cálculo **Eventos**, elija **Actualizar**.
    
3. Para ver los datos de eventos que se recopilan desde las aplicaciones de Office 2013, revise la tabla mostrada en la hoja **Eventos**. 
    
4. Para revisar información acerca del equipo en el cual se han instalado Office 2013 y Registro de telemetría, revise la información mostrada en la hoja **Información del sistema**. 
    
> [!NOTE]
> No es necesario guardar el libro Registro de telemetría en Excel 2013 para mantener un registro de los resultados, pues la información se guarda en el almacén de datos locales (que es independiente de Registro de telemetría). No obstante, guardar el libro no daña el Registro de telemetría. 
  
El Registro de telemetría muestra información sencilla acerca de los eventos registrados. Cada registro mostrado en Registro de telemetría contiene un título y muestra la gravedad del evento mostrado. Para los errores, los registros también incluyen una descripción del error junto con los pasos necesarios para solucionar el problema. Recuerde que no todos los registros mostrados representan errores provocados por las soluciones de Office; el Registro de telemetría también muestra si las soluciones o archivos se cargan o cierran correctamente. 
  
Por ejemplo, el problema llamado "OM oculto: Comment.Initial Property" aparece si una solución o un archivo habilitado para macros abierto en Word 2013 trata de obtener las iniciales de un autor de comentarios asociado con un comentario. Word 2013 cuenta con una experiencia de comentarios mejorada que no muestra las iniciales del autor de comentarios de manera predeterminada. Las API asociadas con el modelo de comentarios anterior se han ocultado en el modelo de objeto de Word 2013, pero siguen estando disponibles para asegurar la compatibilidad con versiones anteriores. El problema "OM oculto: Comment.Initial" de indica el archivo que ha tratado de usar el API, la aplicación que generó el evento (Word 2013), la hora y fecha del evento y una breve descripción del error y el modo de resolverlo.
  
**Figura 1. Registro de telemetría de Office**
  
![El Visor de eventos de Office mostrando registros.](media/off15_OfficeEventViewer_SD.png "El Visor de eventos de Office mostrando registros")
  
> [!NOTE]
>  La hoja de cálculo **Información del sistema** en el Registro de telemetría contiene información sobre el equipo donde está instalado Office 2013. La hoja muestra la siguiente información: 
> - Nombre de usuario.
> - Nombre completo del equipo.
> - Arquitectura del sistema operativo (x64/64 bits o x86/32 bits).
> - Versión de Windows que está instalada en el equipo.
> - Zona horaria del reloj interno del equipo.
> - Versión del Registro de telemetría.
> - Versión de Office que está instalada en el equipo.
> 
> Esta información puede ser útil al interpretar los problemas y eventos que se muestran en la hoja de cálculo **Eventos**. 
  
En Registro de telemetría, se muestra un nivel de gravedad junto con los problemas conocidos. En el ejemplo anterior, un problema en el cual parte del modelo de objeto se ha ocultado suele tener el nivel de gravedad "Informativo". Por otro lado, otros problemas conocidos podrían ser más graves y precisar una acción más inmediata. La gravedad de los problemas mostrados en Registro de telemetría puede ser una de las siguientes:
  
- **Información** El problema podría no tener un efecto inmediato sobre la compatibilidad de la aplicación, pero es posible que el usuario tenga que realizar una acción más tarde. Muchos problemas del tipo "OM oculto" poseen este nivel de gravedad. 
    
- **Aviso** El problema podría provocar la pérdida de datos o suponer una reducción de la fidelidad visual. 
    
- **Crítico**El problema podría provocar una pérdida de funcionalidad significativa o hacer que se bloquee la aplicación. 
    
### <a name="table-2-types-of-events-displayed-in-the-telemetry-log"></a>Tabla 2. Tipos de eventos mostrados en Registro de telemetría
<a name="OEV_Table2"> </a>

Use la siguiente tabla (Tabla 2) para interpretar los registros mostrados en Registro de telemetría.
  
|**Id. de evento**|**Título**|**Gravedad**|**Descripción**|
|:-----|:-----|:-----|:-----|
|1  <br/> |El documento se ha cargado correctamente  <br/> ||El archivo mostrado en la columna **Archivo** se ha abierto en la aplicación de Office sin problemas.  <br/> |
|2  <br/> |No se pudo cargar el documento  <br/> |Advertencia  <br/> | La aplicación no pudo cargar el archivo. Podría haber problemas de compatibilidad subyacentes.  <br/><br/>Para obtener más información sobre cómo reparar un libro dañado en Excel 2013, vea [Reparar un libro dañado](https://office.microsoft.com/en-us/excel-help/repairing-a-corrupted-workbook-HA102749554.aspx).<br/><br/>Para obtener más información sobre cómo reparar un documento dañado en Word 2013, vea [Guardar y recuperar una copia de seguridad de un documento](https://office.microsoft.com/en-us/word-help/save-and-recover-a-backup-copy-of-a-document-HA010121250.aspx). <br/> |
|3  <br/> |La plantilla se ha cargado correctamente  <br/> ||El archivo de plantilla mostrado en la columna **Archivo** se abrió en la aplicación de Office sin ningún problema.  <br/> |
|4  <br/> |No se pudo cargar la plantilla  <br/> |Advertencia  <br/> | La aplicación no pudo cargar el archivo de plantilla. Podría haber problemas de compatibilidad subyacentes o es posible que la disponibilidad de la plantilla haya cambiado.  <br/><br/>Para obtener más información sobre cómo reparar un libro dañado en Excel 2013, vea [Reparar un libro dañado](https://office.microsoft.com/en-us/excel-help/repairing-a-corrupted-workbook-HA102749554.aspx).<br/><br/>Para obtener más información sobre cómo reparar un documento dañado en Word 2013, vea [Guardar y recuperar una copia de seguridad de un documento](https://office.microsoft.com/en-us/word-help/save-and-recover-a-backup-copy-of-a-document-HA010121250.aspx). <br/> |
|5  <br/> |El complemento se ha cargado correctamente  <br/> ||El complemento que aparece en la columna **Archivo** se ha cargado correctamente en la aplicación de Office. No se han detectado problemas de compatibilidad.  <br/> |
|6  <br/> |El complemento no se pudo cargar.  <br/> |Crítico  <br/> | La aplicación no ha podido cargar el complemento que aparece en la columna **Archivo**.  <br/><br/>Para obtener más información sobre cómo reparar un libro dañado en Excel 2013, vea [Reparar un libro dañado](https://office.microsoft.com/en-us/excel-help/repairing-a-corrupted-workbook-HA102749554.aspx). <br/><br/>  Para obtener más información sobre cómo reparar un documento dañado en Word 2013, vea [Guardar y recuperar una copia de seguridad de un documento](https://office.microsoft.com/en-us/word-help/save-and-recover-a-backup-copy-of-a-document-HA010121250.aspx). <br/> |
|7  <br/> |El manifiesto del complemento se descargó correctamente  <br/> ||La aplicación host cargó el manifiesto de la Complemento de Office correctamente.  <br/> |
|8  <br/> |No se pudo descargar el manifiesto del complemento  <br/> |Crítico  <br/> |La aplicación host no pudo cargar el archivo de manifiesto de la Complemento de Office desde el catálogo de SharePoint, el catálogo corporativo o la Tienda Office.  <br/> |
|9  <br/> |No se pudo analizar el manifiesto del complemento  <br/> |Crítico  <br/> |La aplicación host cargó el manifiesto de Complemento de Office del complemento, pero no pudo leer el XML.  <br/> |
|10  <br/> |El complemento usó demasiada CPU  <br/> |Crítico  <br/> |La Complemento de Office usó más del 90 % de los recursos de la CPU durante un período de tiempo limitado.  <br/> |
|11  <br/> |La aplicación se ha bloqueado durante la carga.  <br/> |Crítico  <br/> |La aplicación de Office trató de cargar un documento o solución cuando se inició, pero problemas con el documento o la solución impidieron que se iniciara la aplicación.  <br/> |
|12  <br/> |La aplicación se ha cerrado por un problema  <br/> |Crítico  <br/> |Algo ha provocado un error crítico en la aplicación y debe cerrarse.  <br/> |
|13  <br/> |El documento se ha cerrado correctamente  <br/> ||El archivo que aparece en la columna **Archivo** se ha cerrado correctamente.  <br/> |
|14  <br/> |La sesión de la aplicación se ha ampliado  <br/> ||Las sesiones de aplicaciones con un documento concreto abierto, o una solución, solo deben durar 24 horas. Si una sesión supera las 24 horas, la aplicación host crea una sesión nueva.  <br/> |
|15  <br/> |El complemento se deshabilitó porque se superó el tiempo de espera de búsqueda de cadenas  <br/> ||Los complementos de correo buscan en el mensaje y la línea de asunto de los correos electrónicos para determinar si deben mostrarse con una expresión regular. Outlook 2013 deshabilitó la aplicación de correo que se muestra en la columna **Archivo** porque agotó el tiempo de espera de forma repetida al intentar encontrar una expresión regular.  <br/> |
|16  <br/> |El documento estaba abierto cuando la aplicación se bloqueó.  <br/> |Crítico  <br/> |El archivo que aparece en la columna **Archivo** estaba abierto cuando se bloqueó la aplicación (mostrada en la columna Aplicación). El archivo podría ser o no responsable del bloqueo de la **Aplicación**.  <br/> |
|17  <br/> |El complemento se cerró correctamente  <br/> |Informativos  <br/> |La aplicación pudo cerrar el complemento correctamente.  <br/> |
|18  <br/> |La aplicación se ha cerrado correctamente  <br/> ||La aplicación host pudo cerrar la Complemento de Office correctamente.  <br/> |
|19  <br/> |Error de tiempo de ejecución del complemento.  <br/> |Crítico  <br/> |Se produjo un problema en Complemento de Office que provocó un error. Para más información, vea el registro de alertas de Microsoft Office con el Visor de eventos de Windows en el equipo donde se produjo el error.  <br/> |
|20  <br/> |No se pudieron comprobar las licencias del complemento.  <br/> |Crítico  <br/> |La información de licencias de Complemento de Office no se pudo comprobar y puede haber expirado. Para más información, vea el registro de alertas de Microsoft Office con el Visor de eventos de Windows en el equipo donde se produjo el error.  <br/> |
|Varios  <br/> |"Cambio del comportamiento de OM: ..."  <br/> |Informativos  <br/> |El código de documento habilitado por macro o complemento usa un objeto, un miembro, una colección, una enumeración o una constante que se comporta de manera diferente de las versiones anteriores de Office.<br/><br/> Para obtener más información, vea [Problemas de compatibilidad en Office](compatibility-issues-in-office.md).  <br/> |
|Varios  <br/> |"OM quitado: …"  <br/> |Crítico  <br/> |El código de documento habilitado por macro o complemento utiliza un objeto, un miembro, una colección, una enumeración o una constante que se han eliminado del modelo de objetos.<br/><br/>Para obtener más información, vea [Problemas de compatibilidad en Office](compatibility-issues-in-office.md).  <br/> |
|Varios  <br/> |"OM oculto: …"  <br/> |Informativos  <br/> |El código de documento habilitado por macro o complemento utiliza un objeto, un miembro, una colección, una enumeración o una constante que se ha ocultado en el modelo de objetos.<br/><br/>Para obtener más información, vea [Problemas de compatibilidad en Office](compatibility-issues-in-office.md).  <br/> |
|Varios  <br/> |"Control: …"  <br/> ||El archivo contiene un control que puede no ser compatible con Office 2013 o con el sistema operativo del equipo.<br/><br/>Para obtener más información, vea [Problemas de compatibilidad en Office](compatibility-issues-in-office.md).  <br/> |
   
## <a name="conclusion"></a>Conclusión
<a name="OEV_Conclusion"> </a>

Registro de telemetría proporciona a las grandes empresas, a los usuarios individuales y a los desarrolladores una herramienta sencilla para supervisar sus soluciones de Office más importantes. Con la identificación de soluciones problemáticas de Office antes de una actualización a gran escala, las empresas podrán predecir de forma más razonable el costo de adoptar Office 2013.
  
## <a name="see-also"></a>Vea también
<a name="OEV_Additional"> </a>

- [Centro para desarrolladores de Office](https://msdn.microsoft.com/office/aa905340.aspx)
- [Problemas de compatibilidad en Office](compatibility-issues-in-office.md)
- [Implementar el panel de telemetría de Office](https://technet.microsoft.com/library/f69cde72-689d-421f-99b8-c51676c77717)
- [Centro para desarrolladores de Office](https://msdn.microsoft.com/office/aa905340)
    

