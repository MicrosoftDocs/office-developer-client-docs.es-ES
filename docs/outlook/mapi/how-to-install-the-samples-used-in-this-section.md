---
title: Instalar los ejemplos que se utilizan en esta sección
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397061"
---
# <a name="install-the-samples-used-in-this-section"></a>Instalar los ejemplos que se utilizan en esta sección

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Para instalar la aplicación MFCMAPI y el proyecto de CreateOutlookItemsAddin para ver y ejecutar el código de ejemplo al que hace referencia en los temas de la sección [Creación de elementos de Outlook mediante el uso de MAPI](creating-outlook-items-by-using-mapi.md) , siga estos pasos. 

Para descargar e instalar los ejemplos utilizados en el "uso de MAPI para crear elementos de Outlook" de sección, siga estos pasos.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Para descargar e instalar la aplicación MFCMAPI y abra el proyecto CreateOutlookItemsAddin

1. Descargue la versión actual de la [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) ejecutable a una carpeta en el sistema. 
    
2. Extraiga el archivo MFCMapi.exe en MFCMapi.exe. _versión_zip a una carpeta vacía en la unidad de disco duro.
    
3. Descargue la versión actual del proyecto [CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828) . 
    
4. Extraer todos los archivos en el archivo CreateOutlookItemsAddin.zip a la carpeta donde extrajo el archivo MFCMapi.exe en el paso 2.
    
5. Copie MFCMapi.exe desde la carpeta utilizada en el paso 2 para el directorio de compilación para el proyecto de CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).
    
6. Abra el proyecto de CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) en Visual Studio para examinar el código fuente. Consulte los temas de la sección [Creación de elementos de Outlook mediante el uso de MAPI](creating-outlook-items-by-using-mapi.md) para determinar qué origen de archivos para abrir. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Ejecute el proyecto de CreateOutlookItemsAddin y MFCMAPI

Los siguientes pasos se suponen que ha descargado e instalado la versión actual del ejecutable MFCMAPI y el proyecto CreateOutlookItemsAddin tal como se describe en el procedimiento anterior. Estos pasos incluyen instrucciones para los elementos de menú **Addins** que le permiten crear elementos de Outlook mediante la aplicación de MFCMAPI y el proyecto CreateOutlookItemsAddin. 
  
> [!NOTE]
> La carpeta que seleccione en el paso 8 y el comando que se seleccione en el paso 9, depende del tipo de elemento que se tratan en uno de los temas de la sección [Creación de elementos de Outlook mediante el uso de MAPI](creating-outlook-items-by-using-mapi.md) . 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Para ejecutar la aplicación MFCMAPI y comandos de menú Addins

1. Iniciar Mfcmapi.exe en la carpeta CreateOutlookItemsAddin\Debug que se crea cuando siga las instrucciones de instalación.
    
2. Haga clic en **Aceptar** para cerrar la pantalla de presentación MFCMAPI. 
    
3. En el menú **sesión** , haga clic en **Inicio de sesión y muestra la tabla de almacenamiento**.
    
4. En el cuadro de diálogo **Elegir perfil** , seleccione el perfil correcto y, a continuación, haga clic en **Aceptar**. 
    
5. Haga doble clic en **buzón - _[Nombre de usuario]_ ** en la vista de lista de la tabla de almacenamiento. 
    
6. En la vista de árbol de la carpeta, expanda el nodo raíz. El nombre que se muestra para el nodo raíz varía según el tipo de perfil seleccionado. Normalmente, este nodo se muestra como **raíz - buzón de correo**.
    
7. En la vista de árbol de la carpeta, expanda el nodo que contiene el almacén de información. El nombre que se muestra para este nodo varía según el tipo de perfil seleccionado. Normalmente, este nodo se muestra como **IPM_SUBTREE** o la **Parte superior del almacén de información**.
    
8. Haga doble clic en la carpeta para el tipo de elemento crear. Por ejemplo, para crear una cita, haga clic en la carpeta de **citas** . 
    
9. En el menú **complementos** , haga clic en el comando apropiado para el elemento que se va a crear. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Descargar y ver el código de la aplicación MFCMAPI

Algunos temas de hacer referencia al código de origen desde la propia aplicación MFCMAPI. Los pasos siguientes describen cómo descargar el código fuente MFCMAPI y ver en Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Para descargar y ver el código fuente de la aplicación de MFCMAPI

1. Descargar el código fuente para la versión actual de la aplicación [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) en una carpeta en el sistema. 
    
2. Extraiga los archivos en MFCMAPI - .zip de _conjunto de cambios_a una carpeta vacía en la unidad de disco duro.
    
3. Abra el proyecto de MFCMapi (\ _foldername_\ MFCMapi.vcproj) en Visual Studio para examinar el código fuente.
    
## <a name="see-also"></a>Vea también

- [Crear un elemento de correo simple](how-to-create-a-simple-mail-item.md)
- [Crear un elemento de tarea periódica simple](how-to-create-a-simple-recurrent-task-item.md)
- [Crear un elemento de cita periódica complejo](how-to-create-a-complex-recurrent-appointment-item.md)
- [Leer y analizar un patrón de periodicidad](how-to-read-and-parse-a-recurrence-pattern.md)

