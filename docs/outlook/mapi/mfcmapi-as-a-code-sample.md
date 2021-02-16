---
title: MFCMAPI como un ejemplo de código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356864"
---
# <a name="mfcmapi-as-a-code-sample"></a>MFCMAPI como un ejemplo de código
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El ejemplo MFCMAPI usa la API de mensajería para proporcionar acceso a los almacenes MAPI a través de una interfaz gráfica de usuario. Después de descargar este ejemplo, puede usar los archivos de origen para examinar casos de uso de ejemplo para muchas de las interfaces y referencias MAPI. Para obtener más información, vea [interfaces MAPI](mapi-interfaces.md).
  
|||
|:-----|:-----|
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1  <br/> |
   
### <a name="to-download-mfcmapi"></a>Para descargar MFCMAPI
  
1. En la [página MFCMAPI,](https://codeplex.com/MFCMAPI) haga clic en la **pestaña Código** fuente. 
    
2. En **Recent Check-Ins**, haga **clic en Descargar** para la compilación más reciente. 
    
3. Lea el contrato de licencia y, a continuación, haga clic **en Acepto.**
    
4. En el cuadro de diálogo **Descarga de archivos**, haga clic en **Guardar**. En el **cuadro de diálogo** Guardar como, busque la carpeta en la que desea guardar los archivos de origen y, a continuación, haga clic en **Guardar**.
    
5. En el cuadro **de diálogo Descargar completado,** haga clic **en Abrir carpeta.** También puedes hacer clic **en Cerrar** para cerrar el cuadro de diálogo y buscar los archivos de origen comprimidos en la carpeta en la que los guardaste. 
    
6. Haga clic con el botón secundario en el archivo **\< \> .zip número** de versión MFCMAPI y, a continuación, haga **clic en Extraer todo**. En el cuadro de diálogo que aparece, haga clic en **Extraer** para extraer los archivos en la carpeta que se muestra. También puede hacer clic **en Examinar** para seleccionar o crear una carpeta diferente. 
    
7. Ejecute Visual Studio 2008 como administrador.
    
   > [!NOTE]
   > Si el equipo ejecuta Windows XP, debe haber iniciado sesión como administrador. Si el equipo ejecuta Windows Vista, debe haber iniciado sesión como administrador y debe hacer clic con el botón secundario en el icono de Visual Studio 2008 y, a continuación, hacer clic en Ejecutar como **administrador.** 
  
8. En Visual Studio 2008, haga clic en Archivo **,** seleccione **Abrir** y, a continuación, haga clic en **Proyecto/Solución.**
    
9. Vaya a la ubicación donde guardó el ejemplo, seleccione **MFCMapi.vcproj** y, a continuación, haga clic en **Abrir**.
    
10. On the **Build** menu, click **Build Solution**.
    
11. En el **cuadro de diálogo Guardar archivo** como, haga clic en **Guardar**.
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>Para usar MFCMAPI como ejemplo de código
  
En **el Explorador de** soluciones, expanda el proyecto **MFCMapi** y  examine los archivos de los nodos Archivos de **encabezado,** Archivos de recursos y Archivos de origen para escenarios de programación.  
  
Muchos temas de métodos de la [sección Interfaces MAPI](mapi-interfaces.md) apuntan a archivos de origen MFCMAPI para ejemplos de programación. Por ejemplo, en [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) se le indica que mire la función en el archivo  `CMsgStoreDlg::OnDisplayReceiveFolderTable` MsgStoreDlg.cpp. 
  
## <a name="see-also"></a>Consulte también

- [Ejemplos de MAPI](mapi-samples.md)

