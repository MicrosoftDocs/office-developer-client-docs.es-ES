---
title: Iniciar una sesión MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9e95423a1aa9a04247a70592a797d2395cafecc4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595373"
---
# <a name="starting-a-mapi-session"></a>Iniciar una sesión MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Aunque hay una gran cantidad de trabajo realizado durante la sesión de inicio, las tareas necesarias son mínimas. Gran parte de este trabajo se realiza en la MAPI de procesamiento de las llamadas [MAPIInitialize](mapiinitialize.md) y [MAPILogonEx](mapilogonex.md) . Ambas funciones aceptan marcas como parámetros de entrada para controlar aspectos de la sesión, como control de notificación y la interfaz de usuario. Es importante comprender las consecuencias de la configuración de cada uno de estos marcadores al llamar a **MAPIInitialize** para inicializar las bibliotecas de MAPI y **MAPILogonEx** para iniciar sesión en el subsistema MAPI. 
  
 **Para iniciar una sesión MAPI**
  
1. Llamar a **MAPIInitialize** para inicializar el conjunto estándar de las bibliotecas de MAPI. 
    
2. Si necesita usar las bibliotecas de OLE, llame a la función OLE [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).
    
3. Si necesita usar la biblioteca de utilidades MAPI, llame a [ScInitMapiUtil](scinitmapiutil.md).
    
4. Llame al método **MAPILogonEx** con un perfil válido para iniciar sesión en el subsistema MAPI. **MAPILogonEx** comprueba la configuración de cada uno de los proveedores de servicios en los servicios de mensaje incluidos en el perfil, preguntar al usuario para obtener información adicional, si es necesario y posibles. Una vez completada **MAPILogonEx** , están listos para el servicio de los proveedores de servicio configurado. 
    
## <a name="in-this-section"></a>En esta sección

[Inicializar MAPI](initializing-mapi.md)
  
> Describe cómo inicializar MAPI para una sesión.
    
[Inicializar OLE para MAPI](initializing-ole-for-mapi.md)
  
> Describe las llamadas para realizar en inicializar OLE para su uso con MAPI.
    
[Inicializar las herramientas MAPI](initializing-the-mapi-utilities.md)
  
> Describe cómo inicializar utilidades MAPI.
    
[Iniciar sesión en MAPI](logging-on-to-mapi.md)
  
> Describe cómo las aplicaciones cliente inicie sesión en el sistema de sub MAPI.
    

