---
title: Integrar con Office desde aplicaciones universales de Windows
manager: soliver
ms.date: 02/06/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60b4fa23-0075-4f6a-8bd0-9e53e99432d5
description: Puede integrar aplicaciones de terceros de la plataforma de aplicaciones universales Windows con Excel Mobile, PowerPoint Mobile y Word Mobile. Las aplicaciones universales se integran con aplicaciones Office a través del contratos del selector de archivos de Windows, propiedades de Expando y contratos del Actualizador de archivos en caché.
ms.openlocfilehash: ad04ccc3ceb6e0f1d53e4aebc12cf9724ab8ab66
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388227"
---
# <a name="integrate-with-office-from-windows-universal-apps"></a>Integrar con Office desde aplicaciones universales de Windows

Puede integrar aplicaciones de terceros de la plataforma de aplicaciones universales Windows con Excel Mobile, PowerPoint Mobile y Word Mobile. Las aplicaciones universales se integran con aplicaciones Office a través del [contratos del selector de archivos](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx) de Windows, [propiedades de Expando](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx) y [contratos del Actualizador de archivos en caché](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
Al integrar la aplicación universal con Excel, PowerPoint o Word Mobile, los usuarios pueden abrir documentos Office que proporciona la aplicación, ya sea al buscar desde Office o cuando usan Windows para abrir archivos desde de la aplicación. También pueden guardar el archivo en la aplicación universal, que carga el archivo en su servicio.
  
Los archivos abiertos de este modo aparecen en la lista Recientes de Office, por lo que los usuarios pueden buscarlos y abrirlos fácilmente.
  
Esta integración requiere que la aplicación universal:
    
- Implemente [los contratos de selector de archivos](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx) de Windows.
    
- Represente un almacén de archivos (por ejemplo, una aplicación que permita tener acceso al almacenamiento en la nube).
    
## <a name="expando-properties"></a>Propiedades de Expando

Las aplicaciones universales de Windows pueden usar propiedades de Expando para comunicar información adicional asociada a archivos. Para obtener información sobre cómo hacerlo en Windows, consulte "System.ExpandoProperties" en [StorageItemContentProperties.SavePropertiesAsync](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx).
  
La tabla siguiente describe las propiedades que la aplicación tiene que proporcionar a Office para habilitar escenarios de archivos abiertos. Si no se proporciona esta información, todos los archivos de la aplicación se abren como de solo lectura. Que los usuarios puedan abrir archivos para su edición depende del tipo de licencia de Office que tengan y del tipo de documento que estén intentando abrir.
  
Establezca estas propiedades en el conjunto de propiedades de **System.ExpandoProperties**. 
  
|**Propiedad**|**Descripción**|**Tipo**|**Ejemplo**|
|:-----|:-----|:-----|:-----|
|**AppDisplayName** <br/> |Nombre del proveedor para mostrar al usuario. Aparece en varios lugares de Office, como la lista de documentos recientes.  <br/> |String  <br/> |Contoso  <br/> |
|**MicrosoftOfficeOwnershipType** <br/> |Para licencias, indique si la ubicación de los documentos es personal/de consumidor o de trabajo/de empresa. Los valores permitidos son 1 (personal) y 2 (empresa). Por ejemplo, si el archivo del usuario se almacena en la empresa Contoso, utilice el valor "2" para la empresa.  <br/> |Unit32  <br/> | 1 o 2  <br/> Por ejemplo, si el archivo del usuario se almacena en la empresa Contoso, este archivo debe marcarse como 2 para la empresa.  <br/> |
|**MicrosoftOfficeTermsOfUse** <br/> |Texto legal para declarar que la información proporcionada es válida según las condiciones de uso. Este texto no se muestra al usuario. Es un acuerdo entre el proveedor de la aplicación y Microsoft.  <br/> Consulte el ejemplo que se muestra a continuación:  <br/> | String  <br/> | Acepto los términos que figuran en [https://go.microsoft.com/fwlink/p/?LinkId=528381](third-party-applications-integrating-with-office-mobile-products.md) <br/> |
   
En el ejemplo de código siguiente se muestra cómo establecer estas propiedades.
  
```cs
public static async Task SetExpandoProperties(StorageFile file,... other params ...) 
  { 
     var expandoProperties = new PropertySet(); 
     expandoProperties.Add("AppDisplayName", "Contoso",);  
     // String value. 
     expandoProperties.Add("MicrosoftOfficeOwnershipType", 1);  
     // Unit32 value - 1 (for personal), 2 (for business).  
     expandoProperties.Add("MicrosoftOfficeTermsOfUse", "I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381");   
    // String value. 
          
       var fileProperties = new PropertySet(); 
       fileProperties.Add("System.ExpandoProperties", expandoProperties); 
       await file.Properties.SavePropertiesAsync(fileProperties); 
  } 

```

## <a name="cached-file-updater-contracts"></a>Contratos del Actualizador de archivos en caché

Si la aplicación universal participa en los contratos del Actualizador de archivos en caché, se le notificarán los cambios realizados en el archivo por otra aplicación universal (como Office). Para obtener información sobre cómo hacerlo en Windows, consulte [clase CachedFileUpdater](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
Office usa la opción **AllowOnlyReaders** para abrir los archivos de lectura y escritura que proporciona su aplicación universal a través de los contratos del selector de archivos. Esto significa que otra aplicación no pueden mover, eliminar, cambiar el nombre ni escribir en el archivo, incluidas las suyas mientras el archivo está abierto en Office. Office guardará automáticamente el archivo, establece CachedFileManager.DeferUpdates para evitar la activación de la aplicación hasta que Office cierre el documento o Office suspenda Windows (cuando el usuario cambie a otra aplicación). Cuando Office cierre el archivo, la aplicación podrá escribir en él. 
  
La aplicación debe controlar toda la comunicación con el servicio, incluidas la descarga, la actualización y la carga.
  
En las tablas siguientes se enumeran los parámetros para configurar y controlar las interacciones entre la aplicación y Office.
  
|**Parámetro**|**Descripción**|
|:-----|:-----|
|[ReadActivationMode](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.readactivationmode.aspx) <br/> |Establezca **BeforeAccess** para permitir que la aplicación actualice el archivo antes de enviarlo a Office.  <br/> |
|[WriteActivationMode](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.writeactivationmode.aspx) <br/> |Establezca **ReadOnly** para que el archivo sea de solo lectura. Establezca **AfterWrite** para asegurarse de que CacheFileUpdater activará la aplicación cuando Office acabe con el archivo.  <br/><br/>**NOTA**: Si no establece **AfterWrite**, no se notificará a la aplicación para que cargue los cambios, lo que significa que los cambios del usuario solo serán locales.           |
|[CachedFileOptions.RequireUpdateOnAccess](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileoptions.aspx) <br/> |Establezca esta propiedad para asegurarse de que la aplicación puede actualizar el archivo cuando un usuario tenga acceso a él desde la lista utilizados recientemente.  <br/> |
   
## <a name="invoking-office-from-your-app"></a>Invocar a Office desde la aplicación

Cuando un usuario abre un documento de Office desde la aplicación, el documento se puede abrir en Excel Mobile, PowerPoint Mobile y Word Mobile. Por ejemplo, cuando un usuario selecciona un archivo \*.docx en su aplicación, se inicia Word Mobilecon el archivo \*.docx abierto. La aplicación Office que se abre se basa en la aplicación que el usuario ha asociado con el tipo de archivo.
  
Para abrir un archivo desde la aplicación en Office, le recomendamos que use **LaunchFileAsync()** para iniciar el archivo. No se recomienda utilizar **LaunchUriAsync()** para iniciar el archivo ya que hará que se inicie la aplicación registrada para el esquema URI (el explorador) en lugar de Office. Aunque **LaunchUriAsync()** con la opción **LauncherOptions.ContentType()** puede invocar a Office, en este caso el archivo abierto se marca como temporal y es de solo lectura en Office. 
  
Para obtener más información, consulte [clase Iniciador](https://msdn.microsoft.com/library/windows/apps/windows.system.launcher.aspx).
  
## <a name="temporary-and-read-only-files"></a>Archivos temporales y de solo lectura

Establezca el atributo **FILE_ATTRIBUTE_TEMPORARY** en los archivos temporales y el atributo **FILE_ATTRIBUTE_READONLY** en los archivos de solo lectura en la aplicación. 
  
Los archivos que tienen el conjunto de atributos **FILE_ATTRIBUTE_TEMPORARY** o **FILE_ATTRIBUTE_READONLY** se abren como de solo lectura en Office. **FILE_ATTRIBUTE_TEMPORARY** también impide que el archivo aparezca en la lista de utilizados recientemente. 
  
Para obtener más información sobre los atributos de archivo, consulte [función SetFileAttributes](https://msdn.microsoft.com/library/windows/desktop/aa365535%28v=vs.85%29.aspx).
  
## <a name="other-best-practices"></a>Otros procedimientos recomendados

Para optimizar la coherencia del archivo, por ejemplo cuando hay modificaciones conflictivas o se producen errores, se aplican los siguientes procedimientos recomendados:
  
- Evite guardar conflictos.
    
  - Pause las cargas cuando se produzcan conflictos de servidor para evitar la bifurcación (solo se bifurca cuando Office ya no tiene un archivo abierto para escritura). Normalmente, si un archivo está abierto en la aplicación Office, la aplicación solo se activa cuando Office se cierra o se suspende por Windows.
    
  - Si necesita controlar los conflictos de la interfaz de usuario, implemente notificaciones del sistema. La interfaz de usuario completa no está disponible cuando se suspende Office.
    
- Controle los errores.
    
  - Cuando se libere un bloqueo, notifique a los usuarios del conflicto y proporcione una ruta para resolverlo dentro de la aplicación.
    
## <a name="see-also"></a>Vea también

- [Integración con Office](integrate-with-office.md)   
- [Integrar con Office desde clientes de sincronización de Win32](integrate-with-office-from-win32-sync-clients.md)
    

