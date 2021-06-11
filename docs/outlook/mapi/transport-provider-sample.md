---
title: Ejemplo del proveedor de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356591"
---
# <a name="transport-provider-sample"></a>Ejemplo del proveedor de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este ejemplo se usan archivos y directorios para transmitir y recibir mensajes. Implementa y registra un preprocesador muy simple que anexa una línea de texto a cada mensaje saliente. En el ejemplo se muestra cómo dividir el contenido del mensaje entre el formato de encapsulación neutro de transporte (TNEF) y el texto. También admite todas las opciones de configuración (hojas de propiedades, asistentes y configuración mediante programación) y opciones de mensaje. No admite las interfaces de transporte remoto. 
  
Puede descargar este ejemplo de Outlook de código de la API de mensajería [(MAPI).](https://go.microsoft.com/fwlink/?LinkId=129740)
  
|||
|:-----|:-----|
|Ejecutable:  <br/> |mrxp32.dll  <br/> |
|Directorio de código fuente:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Características compatibles

En este ejemplo se admiten las siguientes características:
  
- Características básicas como el envío, la recepción y el sondeo de nuevos mensajes.
    
- Configuración interactiva y programática.
    
- La **interfaz IMAPIStatus,** excepto para la configuración de propiedades. Para obtener más información, vea la [interfaz IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) 
    
- Seguridad de subprocesos.
    
- Registro de eventos en un archivo de texto. El archivo se limita automáticamente a un tamaño especificado. Todas las sesiones de transporte usan el mismo archivo.
    
## <a name="unsupported-features"></a>Características no admitidas

Este ejemplo no admite la detección asincrónica de mensajes entrantes.
  
 **Para instalar el proveedor de transporte de ejemplo**
  
1. Para descargar el proveedor de transporte de ejemplo, vea [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).
    
2. Busque la carpeta donde guardó los Outlook mapi. Haga clic con el botón secundario en la **carpeta zip OutlookMAPISamples- \< version \> number** y haga clic en Extraer **todo**.
    
3. Haga **clic en** Examinar, seleccione la ubicación donde desea guardar el ejemplo y haga clic en **Extraer**.
    
4. Ejecute Visual Studio 2008.
    
5. En Visual Studio 2008, haga **clic** en Archivo , seleccione Abrir **y,** a continuación, haga clic **en Project/Solución**.
    
6. Vaya a la ubicación donde guardó el ejemplo, haga clic en **mrxp32.vcproj** y, a continuación, haga clic en **Abrir**.
    
7. En el menú **Generar,** haga clic **en Configuration Manager**.
    
8. En el cuadro **de diálogo Administrador** de configuración, vaya  a la fila **mrxp32** y, en la columna Configuración, seleccione **Liberar** y, a continuación, haga clic **en Cerrar**.
    
9. On the **Build** menu, click **Build Solution**.
    
10. En el **cuadro de diálogo Guardar archivo como,** haga clic en **Guardar**.
    
11. En la carpeta donde guardó el ejemplo, haga clic con el botón secundario en el archivo por lotes de instalación y haga clic **en Ejecutar como administrador.**
    
12. En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.
    
    > [!NOTE]
    > **install.bat** copia el .dll a la carpeta de instalación Microsoft Office predeterminada, C:\Archivos de programa\Microsoft Office\Office12\. Si ha instalado productos Office en otra ubicación, haga clic con el botón secundario **eninstall.bat** y haga clic en **Editar**. El archivo se abre en Bloc de notas. Reemplace la ruta de instalación predeterminada por la ruta de instalación usada en el equipo. 
  
 **Para configurar el proveedor de transporte en Outlook**
  
1. En el **menú Herramientas** de Outlook, haga clic en **Cuenta Configuración**.
    
2. En el **cuadro de diálogo Configuración** cuenta, en la pestaña **Correo** electrónico, haga clic en **Nuevo**.
    
3. En **Elegir servicio de correo electrónico,** haga clic en **Otro**, seleccione Transporte de muestra **de MRXP** y, a continuación, haga clic **en Siguiente**.
    
4. En el cuadro de diálogo Configuración de transporte **mrxp** escriba **un nombre para mostrar de usuario**.
    
5. En **Ruta de acceso a la Bandeja de entrada (recurso compartido UNC)** escriba una ruta de carpeta. También puede ser una ruta de acceso a una carpeta local. 
    
    > [!IMPORTANT]
    > Esta ruta debe existir. 
  
6. Haga clic en **Aceptar**.
    
7. En el cuadro **de diálogo Agregar cuenta** de correo electrónico, haga clic en **Aceptar**. Haga clic **en Finalizar** y, a continuación, **en Cerrar**.
    
8. Para empezar a usar la cuenta de MRXP, salga y reinicie Outlook.
    
 **Para usar el ejemplo del proveedor de transporte para enviar un mensaje en Outlook**
  
1. En el **menú Archivo,** haga clic **en Nuevo** y, a continuación, haga clic en Mensaje **de correo**.
    
2. En el **cuadro Para,** escriba el nombre del destinatario con el formato **[MRXP: \< ADDRESS \> ]**. La dirección es el recurso compartido UNC o la ruta de acceso de carpeta local a la bandeja de entrada del destinatario.
    
    > [!NOTE]
    > Si hay dos puntos o barras diagonales inversas en la dirección, debe insertar una barra diagonal inversa antes de cada dos puntos o barra diagonal inversa. Por ejemplo, para enviar correo a [MRXP:C:\Mail\myDir] debe escribir  `[MRXP:C\:\\Mail\\myDir]` . 
  
    > [!IMPORTANT]
    > La dirección del destinatario debe existir. 
  
3. Haga **clic en Cuenta** y, a **continuación, en Transporte de ejemplo de MRXP**.
    
4. Escriba el mensaje y haga clic en **Enviar**. El mensaje se envía mediante el proveedor de transporte MRXP.
    
 **Para usar el ejemplo del proveedor de transporte para recibir un mensaje en Outlook**
  
1. En el **menú Archivo,** haga clic **en Nuevo** y, a continuación, haga clic en Mensaje **de correo**.
    
2. Escriba el mensaje.
    
3. Haga clic **en el Microsoft Office,** haga clic en Guardar como y, a continuación, haga clic en Guardar **como** para guardar el archivo en la carpeta de bandeja de entrada que especificó durante la instalación.  
    
4. En el **cuadro de diálogo** Guardar como, busque el recurso compartido UNC o la carpeta local que establezca como bandeja de entrada. 
    
5. En la **lista desplegable Guardar como** tipo, haga clic Outlook Formato de **mensaje**.
    
6. Escriba un nombre para el archivo y haga clic en **Guardar**.
    
7. El archivo se guarda en la carpeta compartida. El proveedor de transporte MRXP entrega el mensaje a la Bandeja de entrada en Outlook.
    

