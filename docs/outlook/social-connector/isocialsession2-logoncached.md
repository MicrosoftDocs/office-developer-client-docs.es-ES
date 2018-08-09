---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Inicie sesión en el sitio de red social mediante el uso de credenciales almacenadas en caché.
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821133"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="4a47e-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="4a47e-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="4a47e-104">Inicie sesión en el sitio de red social mediante el uso de credenciales almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="4a47e-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="4a47e-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a47e-105">Parameters</span></span>

<span data-ttu-id="4a47e-106">_Configuración_</span><span class="sxs-lookup"><span data-stu-id="4a47e-106">_connectIn_</span></span>
  
> <span data-ttu-id="4a47e-107">[entrada] Una cadena que puede estar vacía o contiene las credenciales de inicio de sesión, según el contexto en el que el OSC está llamando a **LogonCached**.</span><span class="sxs-lookup"><span data-stu-id="4a47e-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="4a47e-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="4a47e-108">_userName_</span></span>
  
> <span data-ttu-id="4a47e-109">[entrada] Una cadena que contiene el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="4a47e-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="4a47e-110">_contraseña_</span><span class="sxs-lookup"><span data-stu-id="4a47e-110">_password_</span></span>
  
> <span data-ttu-id="4a47e-111">[entrada] Una cadena que contiene la contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="4a47e-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="4a47e-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="4a47e-112">_connectOut_</span></span>
  
> <span data-ttu-id="4a47e-113">[out] Una cadena opaca que contiene las credenciales.</span><span class="sxs-lookup"><span data-stu-id="4a47e-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a47e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a47e-114">Remarks</span></span>

<span data-ttu-id="4a47e-115">Se llama a este método de autenticación sólo si **useLogonCached** se establece como **true** en el XML de las **capacidades de** devuelto por [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span><span class="sxs-lookup"><span data-stu-id="4a47e-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="4a47e-116">Outlook Social Connector (OSC) llama a **LogonCached**y le pasa una cadena vacía para la _configuración_ y cadenas de _nombre de usuario_ y _contraseña_ no vacías.</span><span class="sxs-lookup"><span data-stu-id="4a47e-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="4a47e-117">El proveedor usa el _nombre de usuario_ y _contraseña_ para iniciar sesión en la red social y devuelve un parámetro opaco _connectOut_ para el OSC si la autenticación se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="4a47e-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="4a47e-118">Si se produce un error en la autenticación, el proveedor devuelve el error OSC_E_LOGON_FAILURE para el OSC.</span><span class="sxs-lookup"><span data-stu-id="4a47e-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="4a47e-119">El parámetro _connectOut_ es una cadena opaca para el OSC y se pasa para el parámetro de _configuración_ en los intentos posteriores por el OSC para iniciar sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="4a47e-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="4a47e-120">El proveedor debe colocar todas las credenciales en la cadena de _connectOut_ que el proveedor desea el OSC para almacenar a través de conexiones.</span><span class="sxs-lookup"><span data-stu-id="4a47e-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="4a47e-121">El OSC no interpreta la cadena en _connectOut_y cifra la cadena por razones de seguridad antes de almacenarlos en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="4a47e-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a47e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a47e-122">See also</span></span>

- [<span data-ttu-id="4a47e-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a47e-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

