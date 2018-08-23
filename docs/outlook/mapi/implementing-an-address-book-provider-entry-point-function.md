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
ms.openlocfilehash: 68ba23e6ab23ff7306cd1326b73512b1c9f2a0f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579679"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implementar una función de punto de entrada de proveedor de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando una aplicación las llamadas del cliente [MAPILogonEx](mapilogonex.md) para comenzar una sesión con un perfil que contiene el proveedor de libreta de direcciones, MAPI carga el proveedor y todos los demás que forman parte del perfil. MAPI aprende del nombre de la función de punto de entrada de su proveedor mirando en el perfil. Recuerde que esta función no es el mismo que una función de punto de entrada DLL; vea la documentación de **DllMain** en la documentación de Win32. 
  
Hay varias entradas, algunos de los cuales deben aparecer en el archivo de configuración mapisvc.inf, que se incluyen en la sección de perfil de cada proveedor de la libreta de direcciones. En la siguiente tabla se enumera estas entradas de la sección de perfil y si el archivo mapisvc.inf debe incluirlos.
  
|**Entrada de la sección de perfil**|**requisito de MAPISVC.inf**|
|:-----|:-----|
|PR_DISPLAY_NAME = _cadena_ <br/> |Opcional  <br/> |
|PR_PROVIDER_DISPLAY = _cadena_ <br/> |Obligatorio  <br/> |
|PR_PROVIDER_DLL_NAME = _nombre de DLL_ <br/> |Obligatorio  <br/> |
|PR_RESOURCE_TYPE = _largo_ <br/> |Obligatorio  <br/> |
|PR_RESOURCE_FLAGS = _máscara de bits_ <br/> |Opcional  <br/> |
   
Su proveedor de libreta de direcciones puede colocar esta información en un perfil directamente mediante una llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la sección de su perfil o indirectamente mediante la modificación de MAPISVC.INF. Los perfiles se crean utilizando la información pertinente en MAPISVC. INF para los proveedores de servicio seleccionada o servicios de mensaje. Para obtener más información acerca de la organización y el contenido de MAPISVC. INF, vea el [Archivo de formato de MapiSvc.inf](file-format-of-mapisvc-inf.md).
  
El nombre de la función de punto de entrada DLL de su proveedor libreta de direcciones debe ser [ABProviderInit](abproviderinit.md) y debe cumplir con el prototipo de **ABProviderInit** . Realizar las siguientes tareas en función de punto de entrada DLL de su proveedor: 
  
- Comprobar la versión de la interfaz de proveedor de servicios (SPI) para asegurarse de que MAPI está usando una versión que sea compatible con la versión que está usando el proveedor de libreta de direcciones.
    
- Crear una instancia de un objeto de proveedor de la libreta de direcciones.
    
No llame a **MAPIInitialize** o **MAPIUninitialize** en esta función. 
  
La función de punto de entrada DLL crea una instancia de un objeto de proveedor y devuelve a MAPI un puntero a ese objeto. 
  

