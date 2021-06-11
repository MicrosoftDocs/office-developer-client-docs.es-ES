---
title: Ejemplo del proveedor del almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436870"
---
# <a name="message-store-provider-sample"></a>Ejemplo del proveedor del almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El proveedor de almacén PST ajustado de ejemplo usa un proveedor de archivos de carpetas personales (PST) como back-end para almacenar datos. El proveedor del almacén PST ajustado debe usarse junto con la API de replicación. 
  
La API de replicación permite replicar elementos de un repositorio de datos back-end en un almacén pst de Microsoft Outlook. Use la API de replicación para replicar los datos en un almacén DE PST dedicado y realizar un seguimiento del estado de sincronización. Para obtener más información, vea [Acerca de la API de replicación](about-the-replication-api.md).
  
La mayoría de las funciones del proveedor de almacén PST ajustado de muestra pasan sus argumentos directamente al proveedor de PST subyacente. Algunas funciones requieren una implementación especial y se describen en los temas siguientes.
  
|||
|:-----|:-----|
|Ejecutable:  <br/> |WrpPST32.dll  <br/> |
|Directorio de código fuente:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Características compatibles

Este ejemplo admite Microsoft Outlook 2010 64 bits y ahora se ha revisado para Outlook 2013. Vea los siguientes temas para obtener información adicional:
  
- [Información sobre la API de replicación](about-the-replication-api.md)
    
- [Inicializar un proveedor de almacenamiento PST ajustado](initializing-a-wrapped-pst-store-provider.md)
    
- [Iniciar sesión en un proveedor de almacenamiento PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Uso de un proveedor de almacenamiento PST ajustado](using-a-wrapped-pst-store-provider.md)
    
- [Apagar un proveedor de almacenamiento PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Para instalar el proveedor de almacén PST ajustado de ejemplo**
  
1. Para descargar el proveedor de PST ajustado de ejemplo, [vea Descargar el Outlook de MAPI](downloading-the-outlook-mapi-samples.md).
    
2. Busque la carpeta donde guardó la Outlook mapi. Haga clic con el botón secundario en la **carpeta zip OutlookMAPISamples- \< version \> number** y, a continuación, haga clic en Extraer **todo**.
    
3. Haga **clic en** Examinar, seleccione la ubicación donde desea guardar el ejemplo y, a continuación, haga clic en **Extraer**.
    
4. Ejecute Microsoft Visual Studio 2008.
    
5. En Microsoft Visual Studio 2008, haga clic en Archivo **,** seleccione Abrir **y,** a continuación, haga clic **en Project/Solución**.
    
6. Vaya a la ubicación donde guardó el ejemplo, haga clic **en WrapPST.vcproj** y, a continuación, haga clic en **Abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. En el **cuadro de diálogo Guardar archivo como,** haga clic en **Guardar**.
    
9. En la carpeta donde guardó el ejemplo, haga clic con el botón secundario en **el archivoinstall.bat** y, a continuación, haga clic en Ejecutar como **administrador.**
    
10. En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.
    

