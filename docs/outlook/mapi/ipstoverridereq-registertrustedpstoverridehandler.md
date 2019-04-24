---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Última modificación: 24 de febrero de 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279538"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicia el proceso de desbloqueo de un archivo de carpetas personales (. pst).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Parameters

 _pwzDllPath_
  
> a Un puntero a la ruta de acceso de una biblioteca de vínculos dinámicos (DLL) de terceros.
    
 _pvClientData_
  
> a Un puntero a datos de cliente, que el proveedor PST pasará a las llamadas posteriores a la función HrTrustedPSTOverrideHandlerCallback del archivo DLL. El DLL puede usar estos datos del cliente para ayudar a comprobar si el archivo PST debe estar desbloqueado.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada a la función se realizó correctamente.
    
## <a name="remarks"></a>Comentarios

La DLL especificada por el parámetro wzDllPath debe estar firmada con un certificado digital. La DLL también debe exportar una función con la siguiente firma.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Se llama a esta función con un puntero al objeto IMsgStore para el archivo PST, un puntero a un objeto IUnknown que implementa la interfaz IPSTOVERRIDE1 y un puntero a los datos proporcionados originalmente a través de pvClientData.
  
Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para omitir la Directiva PSTDisableGrow en Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Vea también



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

