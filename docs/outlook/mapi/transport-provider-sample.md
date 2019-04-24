---
title: Ejemplo de proveedor de transporte
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
# <a name="transport-provider-sample"></a>Ejemplo de proveedor de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este ejemplo se usan archivos y directorios para transmitir y recibir mensajes. Implementa y registra un preprocesador muy sencillo que anexa una línea de texto a cada mensaje saliente. En el ejemplo se ilustra cómo dividir el contenido de mensajes entre el formato de encapsulación neutro para el transporte (TNEF) y el texto. También admite todas las opciones de configuración (hojas de propiedades, asistentes y configuración de programación) y opciones de mensajes. No es compatible con las interfaces de transporte remoto. 
  
Puede descargar este ejemplo de ejemplos de código de la [API de mensajería de Outlook (MAPI)](https://go.microsoft.com/fwlink/?LinkId=129740).
  
|||
|:-----|:-----|
|Ejecutable  <br/> |mrxp32. dll  <br/> |
|Directorio de código fuente:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Idioma  <br/> |+  <br/> |
|Select  <br/> |Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Características admitidas

Este ejemplo admite las siguientes características:
  
- Características básicas como el envío, la recepción y el sondeo de mensajes nuevos.
    
- Configuración interActiva y mediante programación.
    
- La interfaz **IMAPIStatus** , excepto el valor de la propiedad. Para obtener más información, consulte la interfaz [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . 
    
- Seguridad de subProcesos.
    
- Registro de eventos en un archivo de texto. El archivo se limita automáticamente a un tamaño especificado. Todas las sesiones de transporte usan el mismo archivo.
    
## <a name="unsupported-features"></a>Características no admitidas

Este ejemplo no admite la detección asincrónica de mensajes entrantes.
  
 **Para instalar el proveedor de transporte de ejemplo**
  
1. Para descargar el proveedor de transporte de muestra, consulte [descargar los ejemplos de MAPI de Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Busque la carpeta en la que guardó los ejemplos de MAPI de Outlook. Haga clic con el botón secundario en la carpeta ZIP del **\<\> número de versión OutlookMAPISamples** y haga clic en **extraer todo**.
    
3. Haga clic en **examinar**, seleccione la ubicación en la que desea guardar el ejemplo y haga clic en **extraer**.
    
4. Ejecute Visual Studio 2008.
    
5. En Visual Studio 2008, haga clic en **archivo**, seleccione **abrir**y, a continuación, haga clic en **proyecto o solución**.
    
6. Vaya a la ubicación en la que guardó el ejemplo, haga clic en **mrxp32. vcproj**y, a continuación, haga clic en **abrir**.
    
7. En el menú **generar** , haga clic en **Administrador de configuración**.
    
8. En el cuadro de diálogo **Administrador de configuración** , vaya a la fila **mrxp32** y, en la columna **configuración** , seleccione **Release**y, a continuación, haga clic en **cerrar**.
    
9. On the **Build** menu, click **Build Solution**.
    
10. En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.
    
11. En la carpeta en la que guardó el ejemplo, haga clic con el botón secundario en el archivo por lotes de instalación y haga clic en **Ejecutar como administrador**.
    
12. En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.
    
    > [!NOTE]
    > **install. bat** copia el archivo. dll en la carpeta de instalación predeterminada de Microsoft Office, C:\Archivos de programa\Microsoft Office\Office12\. Si ha instalado productos de Office en otra ubicación, haga clic con el botón secundario en **install. bat** y haga clic en **Editar**. El archivo se abre en el Bloc de notas. Reemplace la ruta de instalación predeterminada por la ruta de instalación usada en el equipo. 
  
 **Para configurar el proveedor de transporte en Outlook**
  
1. En el menú **herramientas** de Outlook, haga clic en configuración de la **cuenta**.
    
2. En el cuadro de diálogo Configuración de la **cuenta** , en la pestaña **correo electrónico** , haga clic en **nuevo**.
    
3. En **elegir servicio de correo electrónico** , seleccione **MRXP transporte de ejemplo**y, a continuación, haga clic en **siguiente**. ****
    
4. En el cuadro de diálogo **configuración de transporte de MRXP** escriba un nombre para mostrar del **usuario**.
    
5. En **ruta de acceso a la bandeja de entrada (recurso compartido UNC)** escriba una ruta de acceso de carpeta. También puede ser una ruta de acceso a una carpeta local. 
    
    > [!IMPORTANT]
    > Esta ruta de acceso debe existir. 
  
6. Haga clic en **Aceptar**.
    
7. En el cuadro de diálogo **Agregar cuenta de correo electrónico** , haga clic en **Aceptar**. Haga clic en **Finalizar** y, a continuación, en **cerrar**.
    
8. Para empezar a usar la cuenta MRXP, salga y reinicie Outlook.
    
 **Para usar el ejemplo de proveedor de transporte para enviar un mensaje en Outlook**
  
1. En el menú **archivo** , haga clic en **nuevo**y, a continuación, haga clic en **mensaje de correo**.
    
2. En el cuadro **para** , escriba el nombre del destinatario con el formato **[MRXP:\<dirección\>]**. La dirección es el recurso compartido UNC o la ruta de acceso de la carpeta local a la bandeja de entrada del destinatario.
    
    > [!NOTE]
    > Si hay dos puntos o barras diagonales inversas en la dirección, debe insertar una barra diagonal inversa antes de cada dos puntos o barra diagonal inversa. Por ejemplo, para enviar correo a [MRXP: C: \Mail\myDir] debe escribir `[MRXP:C\:\\Mail\\myDir]`. 
  
    > [!IMPORTANT]
    > La dirección del destinatario debe existir. 
  
3. Haga clic en **cuenta** y, a continuación, en **MRXP de transporte de ejemplo**.
    
4. Escriba el mensaje y haga clic en **Enviar**. El mensaje se envía mediante el proveedor de transporte MRXP.
    
 **Para usar el ejemplo de proveedor de transporte para recibir un mensaje en Outlook**
  
1. En el menú **archivo** , haga clic en **nuevo**y, a continuación, haga clic en **mensaje de correo**.
    
2. Escriba el mensaje.
    
3. Haga clic en el **botón Microsoft Office**, haga clic en **Guardar como**y, a continuación, haga clic en **Guardar como** para guardar el archivo en la carpeta Bandeja de entrada que especificó durante la instalación. 
    
4. En el cuadro de diálogo **Guardar como** , busque el recurso compartido UNC o la carpeta local que estableció como bandeja de entrada. 
    
5. En el menú desplegable **Guardar como tipo** , haga clic en **formato de mensaje de Outlook**.
    
6. Escriba un nombre para el archivo y haga clic en **Guardar**.
    
7. El archivo se guarda en la carpeta compartida. El proveedor de transporte MRXP entrega el mensaje a la bandeja de entrada de Outlook.
    

