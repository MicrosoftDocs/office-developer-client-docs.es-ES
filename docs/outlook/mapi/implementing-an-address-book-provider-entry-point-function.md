---
title: Implementación de una función de punto de entrada del proveedor de libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409716"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implementación de una función de punto de entrada del proveedor de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando una aplicación cliente llama a [MAPILogonEx](mapilogonex.md) para iniciar una sesión con un perfil que contiene el proveedor de libreta de direcciones, MAPI carga el proveedor y todos los demás que forman parte del perfil. MAPI aprende del nombre de la función de punto de entrada del proveedor mirando en el perfil. Recuerde que esta función no es la misma que una función de punto de entrada dll; consulta la documentación de **DllMain** en la documentación de Win32. 
  
Hay varias entradas, algunas de las cuales deben aparecer en el archivo de configuración mapisvc.inf, que se incluyen en la sección de perfil de cada proveedor de libreta de direcciones. En la tabla siguiente se enumeran estas entradas de sección de perfil y si el archivo mapisvc.inf debe incluirlas o no.
  
|**Entrada de sección de perfil**|**Requisito de mapisvc.inf**|
|:-----|:-----|
|PR_DISPLAY_NAME= _string_ <br/> |Opcional  <br/> |
|PR_PROVIDER_DISPLAY= _string_ <br/> |Obligatorio  <br/> |
|PR_PROVIDER_DLL_NAME= _nombre de archivo DLL_ <br/> |Obligatorio  <br/> |
|PR_RESOURCE_TYPE= _long_ <br/> |Obligatorio  <br/> |
|PR_RESOURCE_FLAGS= máscara _de bits_ <br/> |Opcional  <br/> |
   
El proveedor de libreta de direcciones puede colocar esta información en un perfil directamente llamando al método [IMAPIProp::SetProps](imapiprop-setprops.md) de su sección de perfil o indirectamente modificando MAPISVC.INF. Los perfiles se construyen con la información relevante en MAPISVC. INF para los proveedores de servicios o servicios de mensajes seleccionados. Para obtener más información acerca de la organización y el contenido de MAPISVC. INF, consulta [Formato de archivo de MapiSvc.inf](file-format-of-mapisvc-inf.md).
  
El nombre de la función de punto de entrada DE DLL del proveedor de la libreta de direcciones debe ser [ABProviderInit](abproviderinit.md) y debe cumplir con el prototipo **ABProviderInit.** Realice las siguientes tareas en la función de punto de entrada dll del proveedor: 
  
- Compruebe la versión de la interfaz del proveedor de servicios (SPI) para asegurarse de que MAPI usa una versión compatible con la versión que está usando el proveedor de libreta de direcciones.
    
- Cree una instancia de un objeto de proveedor de libreta de direcciones.
    
No llame a **MAPIInitialize** o **MAPIUninitialize** en esta función. 
  
La función de punto de entrada DLL crea una instancia de un objeto de proveedor y devuelve a MAPI un puntero a ese objeto. 
  

