---
title: Instalar las muestras usadas en esta sección
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345552"
---
# <a name="install-the-samples-used-in-this-section"></a>Instalar las muestras usadas en esta sección

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para instalar la aplicación MFCMAPI y el proyecto CreateOutlookItemsAddin para ver y ejecutar el código de ejemplo al que hacen referencia los temas de la sección Crear elementos de Outlook mediante [MAPI,](creating-outlook-items-by-using-mapi.md) siga estos pasos. 

Para descargar e instalar los ejemplos usados en la sección "Usar MAPI para crear elementos de Outlook", siga estos pasos.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Para descargar e instalar la aplicación MFCMAPI y abrir el proyecto CreateOutlookItemsAddin

1. Descargue la versión actual del [archivo ejecutable MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) en una carpeta del sistema. 
    
2. Extraiga el MFCMapi.exe archivo en MFCMapi.exe. _version_.zip en una carpeta vacía de la unidad de disco duro.
    
3. Descargue la versión actual del [proyecto CreateOutlookItemsAddin.](https://go.microsoft.com/fwlink/?LinkID=127828) 
    
4. Extraiga todos los archivos del archivo CreateOutlookItemsAddin.zip en la carpeta donde extrajo el MFCMapi.exe en el paso 2.
    
5. Copie MFCMapi.exe de la carpeta usada en el paso 2 al directorio de compilación del proyecto CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).
    
6. Abra el proyecto CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) en Visual Studio para examinar el código fuente. Consulte los temas de la sección Crear elementos [de Outlook](creating-outlook-items-by-using-mapi.md) mediante MAPI para determinar qué archivos de origen se abrirán. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Ejecutar MFCMAPI y el proyecto CreateOutlookItemsAddin

En los pasos siguientes se supone que ha descargado e instalado la versión actual del archivo ejecutable MFCMAPI y del proyecto CreateOutlookItemsAddin, tal como se describe en el procedimiento anterior. Estos pasos le guiarán a los elementos de menú **Complementos** que le permiten crear elementos de Outlook mediante la aplicación MFCMAPI y el proyecto CreateOutlookItemsAddin. 
  
> [!NOTE]
> La carpeta que seleccione en el paso 8 y el comando que seleccione en el paso 9 dependen del tipo de elemento que se describe en uno de los temas de la sección Crear elementos de Outlook mediante [MAPI.](creating-outlook-items-by-using-mapi.md) 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Para ejecutar la aplicación MFCMAPI y los comandos del menú Complementos

1. Inicie Mfcmapi.exe en la carpeta CreateOutlookItemsAddin\Debug que se crea al seguir las instrucciones de instalación.
    
2. Haga **clic en Aceptar** para cerrar la pantalla de presentación MFCMAPI. 
    
3. En el menú **Sesión,** haga clic en **Inicio de sesión y mostrar tabla del almacén.**
    
4. En el **cuadro de diálogo** Elegir perfil, seleccione el perfil correcto y, a continuación, haga clic en **Aceptar.** 
    
5. Haga doble clic **en Buzón de correo - _[Nombre de usuario]_** en la vista de lista de la tabla de almacenamiento. 
    
6. En la vista de árbol de carpetas, expanda el nodo raíz. El nombre que se muestra para el nodo raíz varía según el tipo de perfil seleccionado. Normalmente, este nodo se muestra como **raíz - buzón** de correo .
    
7. En la vista de árbol de carpetas, expanda el nodo que contiene el almacén de información. El nombre que se muestra para este nodo varía según el tipo de perfil seleccionado. Normalmente, este nodo se muestra **como IPM_SUBTREE** o En la parte superior del almacén **de información.**
    
8. Haga doble clic en la carpeta para el tipo de elemento que se creará. Por ejemplo, para crear una cita, haga clic en la **carpeta Citas.** 
    
9. En el **menú Complementos,** haga clic en el comando adecuado para el elemento que se va a crear. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Descargar y ver código de la aplicación MFCMAPI

Algunos temas hacen referencia al código fuente de la propia aplicación MFCMAPI. Los siguientes pasos describen cómo descargar el código fuente MFCMAPI y verlo en Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Para descargar y ver el código fuente de la aplicación MFCMAPI

1. Descargue el código fuente de la versión actual de la [aplicación MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) en una carpeta del sistema. 
    
2. Extraiga los archivos de MFCMAPI- _changeset_.zip en una carpeta vacía de la unidad de disco duro.
    
3. Abra el proyecto MFCMapi (\ _foldername_\ MFCMapi.vcproj) en Visual Studio para examinar el código fuente.
    
## <a name="see-also"></a>Consulte también

- [Crear un elemento de correo simple](how-to-create-a-simple-mail-item.md)
- [Crear un elemento de tarea periódica simple](how-to-create-a-simple-recurrent-task-item.md)
- [Crear un elemento de cita periódica compleja](how-to-create-a-complex-recurrent-appointment-item.md)
- [Leer y analizar un patrón de periodicidad](how-to-read-and-parse-a-recurrence-pattern.md)

