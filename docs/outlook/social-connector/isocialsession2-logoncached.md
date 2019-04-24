---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Inicia sesión en el sitio de red social mediante las credenciales almacenadas en caché.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336508"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="f1eb1-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="f1eb1-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="f1eb1-104">Inicia sesión en el sitio de red social mediante las credenciales almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="f1eb1-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="f1eb1-105">Parameters</span></span>

<span data-ttu-id="f1eb1-106">_connecten_</span><span class="sxs-lookup"><span data-stu-id="f1eb1-106">_connectIn_</span></span>
  
> <span data-ttu-id="f1eb1-107">a Una cadena que puede estar vacía o que contiene las credenciales de inicio de sesión, en función del contexto en el que el OSC llama a **LogonCached**.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="f1eb1-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="f1eb1-108">_userName_</span></span>
  
> <span data-ttu-id="f1eb1-109">a Una cadena que contiene el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="f1eb1-110">_ñ_</span><span class="sxs-lookup"><span data-stu-id="f1eb1-110">_password_</span></span>
  
> <span data-ttu-id="f1eb1-111">a Una cadena que contiene la contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="f1eb1-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="f1eb1-112">_connectOut_</span></span>
  
> <span data-ttu-id="f1eb1-113">contempla Una cadena opaca que contiene las credenciales.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1eb1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1eb1-114">Remarks</span></span>

<span data-ttu-id="f1eb1-115">Se llama a este método para la autenticación solo si **useLogonCached** se establece como **true** en el XML de **capacidades** devuelto por [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md).</span><span class="sxs-lookup"><span data-stu-id="f1eb1-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="f1eb1-116">Outlook Social Connector (OSC) llama a **LogonCached**y pasa una cadena vacía para las cadenas de _nombre de usuario_ y _contraseña_ _conectadas_ y no vacías.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="f1eb1-117">El proveedor usa el _nombre de usuario_ y la _contraseña_ para iniciar sesión en la red social y devuelve un parámetro _connectOut_ opaco al OSC si la autenticación es correcta.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="f1eb1-118">Si se produce un error en la autenticación, el proveedor devuelve el error OSC_E_LOGON_FAILURE al OSC.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="f1eb1-119">El parámetro _connectOut_ es una cadena opaca para OSC y se pasa al parámetro connecten __ en los siguientes intentos del OSC para iniciar sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="f1eb1-120">El proveedor debe situar las credenciales en la cadena _connectOut_ que el proveedor desea que el OSC almacene entre las conexiones.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="f1eb1-121">El OSC no interpreta la cadena en _connectOut_y cifra la cadena por motivos de seguridad antes de almacenarla en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="f1eb1-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f1eb1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1eb1-122">See also</span></span>

- [<span data-ttu-id="f1eb1-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1eb1-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

