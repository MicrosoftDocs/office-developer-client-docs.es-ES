---
title: Ejemplo de proveedor de almacén de mensajes
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
# <a name="message-store-provider-sample"></a>Ejemplo de proveedor de almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El proveedor de almacén de archivos PST ajustado de ejemplo usa un proveedor de archivos de carpetas personales (PST) como back-end para almacenar datos. El proveedor de almacén de archivos PST ajustado debe usarse junto con la API de replicación. 
  
La API de replicación permite replicar elementos de un repositorio de datos back-end en un almacén de archivos PST de Microsoft Outlook. La API de replicación se usa para replicar los datos en un almacén de archivos PST dedicado y realizar un seguimiento del estado de sincronización. Para obtener más información, vea [acerca de la API de replicación](about-the-replication-api.md).
  
La mayoría de las funciones del proveedor de almacén de archivos PST ajustado de ejemplo pasan sus argumentos directamente al proveedor de PST subyacente. Algunas funciones requieren una implementación especial y se describen en los siguientes temas.
  
|||
|:-----|:-----|
|Ejecutable  <br/> |WrpPST32. dll  <br/> |
|Directorio de código fuente:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Idioma  <br/> |+  <br/> |
|Select  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Características admitidas

Este ejemplo admite Microsoft Outlook 2010 64-bit y ahora se ha revisado para Outlook 2013. Consulte los siguientes temas para obtener más información:
  
- [Información sobre la API de replicación](about-the-replication-api.md)
    
- [Inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md)
    
- [Inicio de sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Usar un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md)
    
- [Apagar un proveedor de almacén de archivos PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Para instalar el proveedor de almacén de archivos PST ajustado en muestra**
  
1. Para descargar el proveedor de archivos PST ajustado de muestra, consulte [descargar los ejemplos de MAPI de Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Busque la carpeta en la que guardó los ejemplos de MAPI de Outlook. Haga clic con el botón secundario en la carpeta ZIP del **\<\> número de versión OutlookMAPISamples** y, a continuación, haga clic en **extraer todo**.
    
3. Haga clic en **examinar**, seleccione la ubicación en la que desea guardar el ejemplo y, a continuación, haga clic en **extraer**.
    
4. Ejecute Microsoft Visual Studio 2008.
    
5. En Microsoft Visual Studio 2008, haga clic en **archivo**, seleccione **abrir**y, a continuación, haga clic en **proyecto o solución**.
    
6. Vaya a la ubicación en la que guardó el ejemplo, haga clic en **WrapPST. vcproj**y, a continuación, haga clic en **abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.
    
9. En la carpeta donde guardó el ejemplo, haga clic con el botón secundario en el archivo **install. bat** y, a continuación, haga clic en **Ejecutar como administrador**.
    
10. En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.
    

