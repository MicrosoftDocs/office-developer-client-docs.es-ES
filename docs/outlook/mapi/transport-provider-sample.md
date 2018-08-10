---
title: Muestra de proveedor de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1d0538f02f852580c064560460bb8b2ba54a2f65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820923"
---
# <a name="transport-provider-sample"></a>Muestra de proveedor de transporte

  
  
**Hace referencia a**: Outlook 
  
Este ejemplo utiliza los archivos y directorios para transmitir y recibir mensajes. Se implementa y se registra un preprocesador muy simple que anexa una línea de texto a cada mensaje saliente. El ejemplo muestra cómo dividir el contenido de los mensajes entre el formato de encapsulación neutro de transporte (TNEF) y texto. También es compatible con todas las opciones de configuración (hojas de propiedades, asistentes y configuración mediante programación) y las opciones de mensajes. No admite las interfaces de transporte remoto. 
  
Puede descargar este ejemplo de [Ejemplos de código de API de mensajería de Outlook (MAPI)](http://go.microsoft.com/fwlink/?LinkId=129740).
  
|||
|:-----|:-----|
|Archivo ejecutable:  <br/> |mrxp32.dll  <br/> |
|Directorio de origen del código:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Características admitidas

En este ejemplo es compatible con las siguientes características:
  
- Características básicas, como enviar, recibir y para nuevos mensajes de sondeo.
    
- Configuración interactiva y mediante programación.
    
- La interfaz **IMAPIStatus** , excepto por el valor de la propiedad. Para obtener más información, vea el [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz. 
    
- Seguridad de subprocesos.
    
- Registro de eventos en un archivo de texto. El archivo se limita automáticamente a un tamaño especificado. Todas las sesiones de transporte usan el mismo archivo.
    
## <a name="unsupported-features"></a>Características no admitidas

En este ejemplo no es compatible con detección asincrónica de los mensajes entrantes.
  
 **Para instalar al proveedor de transporte de ejemplo**
  
1. Para descargar el proveedor de transporte de ejemplo, consulte [descargar los ejemplos de MAPI de Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Busque la carpeta donde guardó los ejemplos de MAPI de Outlook. Haga clic en el **OutlookMAPISamples -\<número de versión\> ** zip carpeta y haga clic en **Extraer todos**.
    
3. Haga clic en **Examinar**, seleccione la ubicación donde desea guardar el ejemplo y haga clic en **extraer**.
    
4. Ejecute Visual Studio 2008.
    
5. En Visual Studio 2008, haga clic en **archivo**, seleccione **Abrir**y, a continuación, haga clic en **Proyecto o solución**.
    
6. Vaya a la ubicación donde guardó el ejemplo, haga clic en **mrxp32.vcproj**y, a continuación, haga clic en **Abrir**.
    
7. En el menú **Generar** , haga clic en **Administrador de configuración**.
    
8. En el cuadro de diálogo **Administrador de configuración** , vaya a la fila **mrxp32** y en la columna **configuración** , seleccione **versión**y, a continuación, haga clic en **Cerrar**.
    
9. On the **Build** menu, click **Build Solution**.
    
10. En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.
    
11. En la carpeta donde guardó el ejemplo, haga clic en el archivo por lotes de instalación y haga clic en **Ejecutar como administrador**.
    
12. En el cuadro de diálogo **Control de cuentas de usuario** , haga clic en **continuar**.
    
    > [!NOTE]
    > **Install.bat** copia el archivo .dll en la carpeta de instalación de Microsoft Office de forma predeterminada, C:\Program Files\Microsoft Office\Office12\. Si ha instalado productos de Office en una ubicación diferente, haga clic en **install.bat** y haga clic en **Editar**. El archivo se abre en el Bloc de notas. Reemplace la ruta de instalación predeterminada con la ruta de instalación utilizada en el equipo. 
  
 **Para configurar el proveedor de transporte en Outlook**
  
1. En el menú **Herramientas** de Outlook, haga clic en **Configuración de la cuenta**.
    
2. En el cuadro de diálogo **Configuración de la cuenta** , en la ficha **correo electrónico** , haga clic en **nuevo**.
    
3. En **Elegir servicio de correo electrónico** haga clic en **otros**, seleccione **MRXP ejemplo de transporte**y, a continuación, haga clic en **siguiente**.
    
4. En el cuadro de diálogo **Configuración de transporte MRXP** escriba un **Nombre de usuario para mostrar**.
    
5. En la **ruta de acceso a la Bandeja de entrada (recurso compartido UNC)** , escriba una ruta de acceso de la carpeta. Esto también puede ser una ruta de acceso a una carpeta local. 
    
    > [!IMPORTANT]
    > Esta ruta de acceso debe existir. 
  
6. Haga clic en **Aceptar**.
    
7. En el cuadro de diálogo **Agregar una cuenta de correo electrónico** , haga clic en **Aceptar**. Haga clic en **Finalizar** y, a continuación, haga clic en **Cerrar**.
    
8. Para empezar a usar la cuenta de MRXP, salga y reinicie Outlook.
    
 **Para usar el ejemplo de proveedor de transporte para enviar un mensaje en Outlook**
  
1. En el menú **archivo** , haga clic en **nuevo**y, a continuación, haga clic en **El mensaje de correo**.
    
2. En **el cuadro** escriba el nombre del destinatario con el formato **[MRXP:\<dirección\>]**. La dirección es el recurso compartido UNC o una ruta de acceso de carpeta local a la Bandeja de entrada del destinatario.
    
    > [!NOTE]
    > Si hay dos puntos o barras diagonales inversas en la dirección, debe insertar una barra diagonal inversa antes de cada carácter de dos puntos o una barra diagonal inversa. Por ejemplo, para enviar correo a [MRXP:C:\Mail\myDir] debe que escribir `[MRXP:C\:\\Mail\\myDir]`. 
  
    > [!IMPORTANT]
    > Debe existir la dirección del destinatario. 
  
3. Haga clic en **cuenta** y, a continuación, haga clic en **Transporte de ejemplo MRXP**.
    
4. Escriba el mensaje y haga clic en **Enviar**. El mensaje se envía con el proveedor de transporte MRXP.
    
 **Para usar el ejemplo de proveedor de transporte para recibir un mensaje en Outlook**
  
1. En el menú **archivo** , haga clic en **nuevo**y, a continuación, haga clic en **El mensaje de correo**.
    
2. Escriba el mensaje.
    
3. Haga clic en el **Botón de Microsoft Office**, haga clic en **Guardar como**y, a continuación, haga clic en **Guardar como** para guardar el archivo en la carpeta Bandeja de entrada especificados durante la instalación. 
    
4. En el cuadro de diálogo **Guardar como** , busque el recurso compartido UNC o una carpeta local que ha configurado como la Bandeja de entrada. 
    
5. En la lista **Guardar como tipo** desplegable, haga clic en **Formato de mensaje de Outlook**.
    
6. Escriba un nombre para el archivo y haga clic en **Guardar**.
    
7. El archivo se guarda en la carpeta compartida. El proveedor de transporte MRXP entrega el mensaje a la Bandeja de entrada en Outlook.
    

