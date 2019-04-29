---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405089"
---
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Instala un formulario en una biblioteca de formularios.
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método. El parámetro _ulUIParam_ se omite a menos que la aplicación cliente establezca la marca MAPI_DIALOG en el parámetro _ulFlags_ . El parámetro _ulUIParam_ puede ser null si MAPI_DIALOG no se pasa también. 
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla la instalación del formulario. Se pueden establecer los siguientes indicadores:
    
MAPI_DIALOG 
  
> Muestra un cuadro de diálogo para proporcionar información de progreso o solicitar información al usuario. Si no se establece esta marca, no se muestra ningún cuadro de diálogo.
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Si ya existe otro formulario que controla la clase de mensaje controlada por este formulario, reemplace el formulario existente por éste. Esta marca se pasa por alto si la marca MAPI_DIALOG también está presente. 
    
 _szCfgPathName_
  
> a Ruta de acceso al archivo de configuración del formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_EXTENDED_ERROR 
  
> Se ha producido un error de implementación. Para obtener la estructura [MAPIERROR](mapierror.md) asociada con el error, llame al método [IMAPIFormContainer:: GetLastError](imapiformcontainer-getlasterror.md) . 
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la instalación del formulario, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Los proveedores de bibliotecas de formularios deben rellenar una estructura **MAPIERROR** y devolver MAPI_E_EXTENDED_ERROR si se produce alguna de las condiciones siguientes: 
  
- No se encuentra el archivo de configuración.
    
- No se puede leer el archivo de configuración.
    
- El archivo de configuración no es válido.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Las aplicaciones cliente llaman al método **IMAPIFormContainer:: InstallForm** para instalar un formulario en un contenedor de formulario específico. El parámetro _szCfgPathName_ debe contener la ruta de acceso de un archivo de configuración de formulario (es decir, un archivo con la extensión. cfg que describe el formulario y su implementación). Las marcas del parámetro _ulFlags_ especifican lo siguiente: 
  
- Si se establece la marca MAPI_DIALOG, se muestra una interfaz de usuario, que permite al usuario que está instalando el formulario especificar los detalles de la instalación.
    
- Si se establece la marca MAPIFORM_INSTALL_OVERWRITEONCONFLICT, cualquier formulario anterior para la misma clase de mensaje se reemplaza por el formulario que se está instalando. De lo contrario, la instalación del formulario se combina con la descripción del formulario actual, si existe alguna.
    
- Si se establece MAPI_DIALOG, se omitirá MAPIFORM_INSTALL_OVERWRITEONCONFLICT.
    
- La ausencia de MAPIFORM_INSTALL_OVERWRITEONCONFLICT en el conjunto de marcas significa que se realizará una combinación. Todas las plataformas nuevas del archivo. cfg que no se encuentren actualmente en la descripción del formulario se instalarán y no se producirá ningún otro cambio.
    
- Si se establece la marca MAPI_UNICODE, la ruta de acceso del archivo de configuración de formulario es una cadena Unicode. 
    
Los clientes deben llamar a [IMAPIFormContainer:: GetLastError](imapiformcontainer-getlasterror.md) si **InstallForm** devuelve MAPI_E_EXTENDED_ERROR y deben comprobar la estructura devuelta de [MAPIERROR](mapierror.md) para determinar la condición que generó el error. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnInstallForm  <br/> |MFCMAPI usa el método **IMAPIFormContainer:: InstallForm** para instalar un formulario en un contenedor de formularios.  <br/> |
   
## <a name="see-also"></a>Ver también



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

