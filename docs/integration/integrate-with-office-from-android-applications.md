---
title: Integración con Office desde aplicaciones de Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office para Android proporciona una solución extensible que permite la integración con aplicaciones de terceros. Puede integrarse con Office desde su aplicación de Android pasando usuarios de la aplicación a Office.
ms.openlocfilehash: 4e674b3d66f3acba7e9c9c19e716ff0d73d803b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393029"
---
# <a name="integrate-with-office-from-android-applications"></a>Integración con Office desde aplicaciones de Android

Office para Android proporciona una solución extensible que permite la integración con aplicaciones de terceros. Puede integrarse con Office desde su aplicación de Android pasando usuarios de la aplicación a Office.
  
Puede permitir que los usuarios que ejecutan Office en un dispositivo Android abran y editen los archivos almacenados en SharePoint o OneDrive desde cualquier aplicación. Para ello, pase archivos a Office mediante controladores de protocolo y asegúrese de que Office se invoca de tal manera que Office pueda entender.
  
Cuando un usuario termina de editar un archivo, puede elegir la tecla Atrás en el dispositivo para volver a la aplicación de almacenamiento original.
  
## <a name="verify-that-office-has-been-installed"></a>Compruebe que se haya instalado Office.

La aplicación de referencia deberá comprobar primero que una determinada aplicación de Office está instalada. Las siguientes aplicaciones de Office se pueden instalar en dispositivos Android para la visualización y edición de documentos: 
  
- Excel
    
- PowerPoint
    
- Word
    
Use PackageManager de Android para determinar si una aplicación determinada de Office está instalada en el dispositivo. En la siguiente tabla se enumeran los nombres de paquete para las aplicaciones de Office que puede usar en este proceso.
  
|**Aplicación**|**Nombre del paquete**|
|:-----|:-----|
|Excel  <br/> |com.microsoft.office.excel  <br/> |
|PowerPoint  <br/> |com.microsoft.office.powerpoint  <br/> |
|Word  <br/> |com.microsoft.office.word  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a>Solicitar al usuario que instale Office

Si una aplicación determinada de Office no está instalada, puede solicitar al usuario que la instale. En la siguiente tabla se enumeran las ubicaciones de instalación disponibles para las aplicaciones de Office.
  
|**Aplicación**|**Google Play Store**|
|:-----|:-----|
|Excel  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|PowerPoint  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|Word  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a>Invocar a Office

Cuando la aplicación de Office está instalada, la aplicación de referencia puede invocar a Office pasando los siguientes detalles:
  
- Protocolo de Office
    
- Modo de apertura
    
- URL
    
Formato de esquema:
  
 `<Office protocol><open mode>|u|<URL>`
  
El siguiente ejemplo muestra una solicitud para invocar un archivo de Word para su edición:
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a>Protocolos de Office

La siguiente tabla enumera los protocolos para cada aplicación de Office.
  
|**Aplicación**|**Protocolo**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
|PowerPoint  <br/> |ms-powerpoint:  <br/> |
|Word  <br/> |ms-word:  <br/> |
   
### <a name="open-mode"></a>Modo de apertura

Las aplicaciones de Office pueden abrir archivos directamente en el modo de visualización (ofv) o edición (ofe). El modo de edición es el predeterminado.
  
Formato de esquema:
  
 `<ofv or ofe>`
  
### <a name="url"></a>URL

La dirección URL incluye tres partes:
  
- La declaración de que el archivo se abrirá para su edición (ofe)
    
- El descriptor de la dirección URL (|u|)
    
- La dirección URL
    
La dirección URL se debe codificar y debe ser un vínculo directo al archivo (no una redirección). Si la dirección URL está en un formato que Office no puede gestionar o simplemente se produce un error en la descarga, Office no devolverá al usuario a la aplicación que realizó la invocación.
  
Formato de esquema:
  
 `|u|<document URL>`
  
## <a name="see-also"></a>Vea también
<a name="bk_addresources"> </a>

- [Integración con Office](integrate-with-office.md)
    
- [PackageManager](https://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [GetPackageManager()](https://developer.android.com/reference/android/content/Context.html)
    

