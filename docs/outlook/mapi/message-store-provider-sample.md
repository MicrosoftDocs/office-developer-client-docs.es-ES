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
ms.openlocfilehash: 25c606531aa9a7436306a1b87c32aab49fd975db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593917"
---
# <a name="message-store-provider-sample"></a>Ejemplo de proveedor de almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El proveedor de almacén de archivos PST ajustado de ejemplo usa un proveedor de carpetas personales (PST) de archivo como back-end para almacenar los datos. El proveedor de almacén de archivos PST ajustado debe usarse junto con la API de replicación. 
  
La API de replicación permite replicar los elementos de un repositorio de datos de back-end en un almacén de archivos PST de Microsoft Outlook. Usar la API de replicación para replicar los datos en un almacén de archivos PST dedicado y realizar un seguimiento de estado de sincronización. Para obtener más información, vea [Acerca de la API de replicación](about-the-replication-api.md).
  
La mayoría de las funciones en el proveedor de almacén de archivos PST ajustado de ejemplo pasa sus argumentos directamente al proveedor de PST subyacente. Ciertas funciones requieren implementación especial y se describen en los temas siguientes.
  
|||
|:-----|:-----|
|Archivo ejecutable:  <br/> |WrpPST32.dll  <br/> |
|Directorio de origen del código:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Características admitidas

En este ejemplo es compatible con Microsoft Outlook 2010 de 64 bits y ahora se ha revisado para Outlook 2013. Consulte los siguientes temas para obtener información adicional:
  
- [Información sobre la API de replicación](about-the-replication-api.md)
    
- [Inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md)
    
- [Iniciar sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Usar un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md)
    
- [Apagar un proveedor de almacén de archivos PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Para instalar al proveedor de almacén de archivos PST ajustado de ejemplo**
  
1. Para descargar el proveedor de PST ajustado de ejemplo, consulte [descargar los ejemplos de MAPI de Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Busque la carpeta donde guardó los ejemplos de MAPI de Outlook. Haga clic en el **OutlookMAPISamples -\<número de versión\> ** zip de carpeta y, a continuación, haga clic en **Extraer todos**.
    
3. Haga clic en **Examinar**, seleccione la ubicación donde desea guardar el ejemplo y, a continuación, haga clic en **extraer**.
    
4. Ejecute Microsoft Visual Studio 2008.
    
5. En Microsoft Visual Studio 2008, haga clic en **archivo**, seleccione **Abrir**y, a continuación, haga clic en **Proyecto o solución**.
    
6. Vaya a la ubicación donde guardó el ejemplo, haga clic en **WrapPST.vcproj**y, a continuación, haga clic en **Abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.
    
9. En la carpeta donde guardó el ejemplo, haga clic en el archivo **install.bat** y, a continuación, haga clic en **Ejecutar como administrador**.
    
10. En el cuadro de diálogo **Control de cuentas de usuario** , haga clic en **continuar**.
    

