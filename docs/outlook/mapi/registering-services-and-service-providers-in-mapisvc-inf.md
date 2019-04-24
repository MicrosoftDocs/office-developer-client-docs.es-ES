---
title: Registrar servicios y proveedores de servicios en MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Última modificación: 18 de julio de 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328374"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Registrar servicios y proveedores de servicios en MapiSvc. inf

 
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Para instalar un nuevo proveedor en un sistema, es necesario actualizar el archivo MapiSvc. inf para que apunte al nuevo proveedor. Las propiedades estándar establecidas durante la configuración, entre las que se incluyen las siguientes, informan a MAPI dónde encontrar la biblioteca de vínculos dinámicos del proveedor (. dll):
  
- La **PR_SERVICE_DLL_NAME** se especifica en la sección **[Message Service]** . 
    
- La **PR_PROVIDER_DLL_NAME** se especifica en la sección **[proveedor de servicios]** . 
    
> [!NOTE]
> La expectativa es que establezca el nombre del archivo. dll de su proveedor (sin el sufijo "32"). MAPI, a continuación, carga el proveedor buscándolo en la ruta de acceso. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Poner una ruta de acceso en MapiSvc. inf

La mayoría de las aplicaciones se instalan en archivos de programa, lo que requiere una actualización a la variable PATH para permitir que los proveedores MAPI funcionen. Con algunas restricciones, Microsoft Outlook 2010 y Outlook 2013 pueden admitir rutas completas a los proveedores MAPI.
  
Al registrar el proveedor en MapiSvc. inf, puede incluir la ruta de acceso completa en el proveedor en las propiedades MAPI **PR_SERVICE_DLL_NAME** y **PR_PROVIDER_DLL_NAME**.
  
En cualquiera de las dos propiedades, la ruta de acceso completa debe estar sin el sufijo "32", ya que MAPI continuará anexando esa al nombre de archivo antes de buscar el archivo. Esto significa que si registra la ruta "c:\mypath\myprovider.dll", MAPI intentará cargar "c:\mypath\myprovider32.dll".
  
Como MAPI de Outlook no se diseñó originalmente para dar cabida a rutas de todas las rutas, realiza esta inserción del sufijo "32" buscando el primer punto de la cadena, lo que significa que las rutas que contienen otros períodos no pueden funcionar, por lo que no puede usar rutas como "c:\my.path\myprovider.dll" o "c:\mypath\my.Provider.dll".
  
A veces, en un proveedor de almacenamiento generará identificadores de entrada mediante la función **WrapStoreEntryID** , que toma como parámetro el nombre de su proveedor. 
  
> [!IMPORTANT]
> Si está usando rutas completas en MapiSvc. inf, debe usar la misma ruta de acceso en cualquier llamada a **WrapStoreEntryID**. 
  
Además, la ruta de acceso que use se puede convertir a y desde Unicode mediante la página de códigos proporcionada por la función [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) . 
  
> [!CAUTION]
> Experimentará un error si elige una ruta de acceso que contiene caracteres que no pueden sobrevivir a este tipo de ida y vuelta a través de las funciones [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) y [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) . 
  
Para una demostración de esta funcionalidad, se ha revisado el [ejemplo de PST ajustado](https://github.com/stephenegriffin/Outlook2010CodeSamples) en github: la funcionalidad correspondiente está en **MergeWithMapiSvc** y **GenerateProviderPath**.
  

