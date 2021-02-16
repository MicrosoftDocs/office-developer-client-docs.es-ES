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

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método. El _parámetro ulUIParam_ se omite a menos que la aplicación cliente MAPI_DIALOG marca en el _parámetro ulFlags._ El  _parámetro ulUIParam_ puede ser NULL si MAPI_DIALOG no se pasa. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla la instalación del formulario. Se pueden establecer las siguientes marcas:
    
MAPI_DIALOG 
  
> Muestra un cuadro de diálogo para proporcionar información de progreso o solicitar al usuario más información. Si no se establece esta marca, no se muestra ningún cuadro de diálogo.
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Si ya existe otro formulario que controla la clase de mensaje que controla este formulario, reemplace el formulario existente por este. Esta marca se omite si la MAPI_DIALOG también está presente. 
    
 _szCfgPathName_
  
> [entrada] Ruta de acceso al archivo de configuración del formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_EXTENDED_ERROR 
  
> Se produjo un error de implementación. Para obtener la [estructura MAPIERROR](mapierror.md) asociada al error, llame al método [IMAPIFormContainer::GetLastError.](imapiformcontainer-getlasterror.md) 
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la instalación del formulario, normalmente haciendo clic en el **botón** Cancelar de un cuadro de diálogo. 
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Los proveedores de bibliotecas de formularios deben rellenar una **estructura MAPIERROR** y devolver MAPI_E_EXTENDED_ERROR si se produce alguna de las siguientes condiciones: 
  
- No se encuentra el archivo de configuración.
    
- El archivo de configuración no es legible.
    
- El archivo de configuración no es válido.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Las aplicaciones cliente llaman **al método IMAPIFormContainer::InstallForm** para instalar un formulario en un contenedor de formulario específico. El  _parámetro szCfgPathName_ debe contener la ruta de acceso de un archivo de configuración de formulario (es decir, un archivo con la extensión .cfg que describe el formulario y su implementación). Las marcas del parámetro  _ulFlags_ especifican lo siguiente: 
  
- Si se MAPI_DIALOG marca, se muestra una interfaz de usuario, lo que permite al usuario que está instalando el formulario especificar los detalles de instalación.
    
- Si se MAPIFORM_INSTALL_OVERWRITEONCONFLICT marca, cualquier formulario anterior para la misma clase de mensaje se reemplaza por el formulario que se está instalando. De lo contrario, la instalación del formulario se combina con la descripción del formulario actual, si existe.
    
- Si MAPI_DIALOG se establece, MAPIFORM_INSTALL_OVERWRITEONCONFLICT se omite.
    
- La ausencia de MAPIFORM_INSTALL_OVERWRITEONCONFLICT en el conjunto de marcas significa que se realizará una combinación. Se instalarán las nuevas plataformas del archivo .cfg que no estén presentes actualmente en la descripción del formulario y no se producirán otros cambios.
    
- Si se MAPI_UNICODE marca, la ruta de acceso del archivo de configuración del formulario es una cadena Unicode. 
    
Los clientes deben llamar a [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) si **InstallForm** devuelve MAPI_E_EXTENDED_ERROR y deben comprobar la estructura [MAPIERROR](mapierror.md) devuelta para determinar la condición que ha producido el error. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI usa el **método IMAPIFormContainer::InstallForm** para instalar un formulario en un contenedor de formularios.  <br/> |
   
## <a name="see-also"></a>Consulte también



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

