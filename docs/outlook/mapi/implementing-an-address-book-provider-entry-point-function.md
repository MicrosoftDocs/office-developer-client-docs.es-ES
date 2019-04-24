---
title: Implementar una función de punto de entrada de proveedor de libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332805"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implementar una función de punto de entrada de proveedor de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando una aplicación de cliente llama a [MAPILogonEx](mapilogonex.md) para iniciar una sesión con un perfil que contiene el proveedor de la libreta de direcciones, MAPI carga el proveedor y el resto de los elementos que forman parte del perfil. MAPI aprende el nombre de la función de punto de entrada de su proveedor al buscar en el perfil. Recuerde que esta función no es la misma que una función de punto de entrada de DLL; Vea la documentación de **DllMain** en la documentación de Win32. 
  
Hay varias entradas, algunas de las cuales deben aparecer en el archivo de configuración MAPISVC. inf, que se incluyen en la sección de Perfil de todos los proveedores de la libreta de direcciones. En la siguiente tabla se enumeran estas entradas de sección de perfil y si el archivo MAPISVC. inf debe incluirlas o no.
  
|**Entrada de sección de perfil**|**requisito de MAPISVC. inf**|
|:-----|:-----|
|PR_DISPLAY_NAME = _String_ <br/> |Opcional  <br/> |
|PR_PROVIDER_DISPLAY = _String_ <br/> |Obligatorio  <br/> |
|PR_PROVIDER_DLL_NAME = _nombre_ de archivo dll <br/> |Obligatorio  <br/> |
|PR_RESOURCE_TYPE = _Long_ <br/> |Obligatorio  <br/> |
|PR_RESOURCE_FLAGS = _máscara_ de <br/> |Opcional  <br/> |
   
El proveedor de la libreta de direcciones puede incluir esta información en un perfil directamente llamando al método [IMAPIProp:: SetProps](imapiprop-setprops.md) de la sección del perfil o indirectamente modificando MAPISVC. inf. Los perfiles se crean con la información relevante en MAPISVC. INF para los proveedores de servicios o los servicios de mensajes seleccionados. Para obtener más información acerca de la organización y el contenido de MAPISVC. INF, consulte [formato de archivo de MapiSvc. inf](file-format-of-mapisvc-inf.md).
  
El nombre de la función de punto de entrada de DLL del proveedor de la libreta de direcciones debe ser [ABProviderInit](abproviderinit.md) y debe cumplir con el prototipo **ABProviderInit** . Realice las siguientes tareas en la función de punto de entrada de DLL del proveedor: 
  
- Compruebe la versión de la interfaz del proveedor de servicios (SPI) para asegurarse de que MAPI está usando una versión compatible con la versión que el proveedor de la libreta de direcciones usa.
    
- Crear una instancia de un objeto de proveedor de libreta de direcciones.
    
No llame a **MAPIInitialize** o **MAPIUninitialize** en esta función. 
  
La función de punto de entrada de DLL crea una instancia de un objeto de proveedor y devuelve a MAPI un puntero a ese objeto. 
  

