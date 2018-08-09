---
title: Constantes (API de administración de cuenta)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2a15e5df-b8e3-9c37-b1ee-2881d010e30b
description: Este tema contiene las definiciones de constantes, los identificadores de clase y los identificadores de interfaz para la API de administración de cuentas.
ms.openlocfilehash: b9db04e8847748375f4958855a5813e050b1047b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816087"
---
# <a name="constants-account-management-api"></a>Constantes (API de administración de cuenta)

Este tema contiene las definiciones de constantes, los identificadores de clase y los identificadores de interfaz para la API de administración de cuentas.
  
## <a name="constants"></a>Constantes

|**Constante**|**Definición**|
|:-----|:-----|
|ACCT_INIT_NOSYNCH_MAPI_ACCTS  <br/> |0x00000001  <br/> |
|ACCT_INIT_NO_STORES_CHECK  <br/> |0x00000002  <br/> |
|ACCTUI_NO_WARNING  <br/> |0 x 0100  <br/> |
|ACCTUI_SHOW_ACCTWIZARD  <br/> |0 x 0400  <br/> |
|ACCTUI_SHOW_DATA_TAB  <br/> |0 x 0200  <br/> |
|E_ACCT_NOT_FOUND  <br/> |0x800C8101  <br/> |
|E_ACCT_UI_BUSY  <br/> |0x800C8102  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |0x800C8105  <br/> |
|E_INVALIDARG  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Kit de desarrollo de Software (SDK) de Windows.*  <br/> |
|E_NOTIMPL  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Windows SDK.*  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |0x800C8002  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |0x800C8005  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |0x800C8003  <br/> |
|E_OLK_PROP_READ_ONLY  <br/> |0x800C800D  <br/> |
|E_OLK_REGISTRY  <br/> |0x800C8001  <br/> |
|Las siguientes constantes que comiencen por ENCRYPT_ se usan por la propiedad [PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) para especificar el tipo de conexión cifrada.  <br/> ||
|ENCRYPT_CONN_AUTO  <br/> |3  <br/> |
|ENCRYPT_CONN_NO_SECURITY  <br/> |0  <br/> |
|ENCRYPT_CONN_SSL  <br/> |1  <br/> |
|ENCRYPT_CONN_TLS  <br/> |2  <br/> |
|MAPIACCT_SEND_ONLY  <br/> |0x00000001  <br/> |
|NOTIFY_ACCT_CHANGED  <br/> |1  <br/> |
|NOTIFY_ACCT_CREATED  <br/> |2  <br/> |
|NOTIFY_ACCT_DELETED  <br/> |3  <br/> |
|NOTIFY_ACCT_ORDER_CHANGED  <br/> |4  <br/> |
|NOTIFY_ACCT_PREDELETED  <br/> |5  <br/> |
|OLK_ACCOUNT_NO_FLAGS  <br/> |0  <br/> |
|S_OK  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Windows SDK.*  <br/> |
|S_FALSE  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Windows SDK.*  <br/> |
|SECURE_FLAG  <br/> |0 x 8000  <br/> |
|Las siguientes constantes que comiencen por SMTP_ se usan por la propiedad [PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) y especifican el método de autenticación.  <br/> ||
|SMTP_AUTH_SAME_AS_POP  <br/> |0  <br/> |
|SMTP_AUTH_RECEIVE_BEFORE_SEND  <br/> |2  <br/> |
|SMTP_AUTH_USER_PASS  <br/> |1  <br/> |
|Las siguientes 5 constantes y las macros se usan por la propiedad [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) y especifican las opciones para las cuentas POP dejar una copia de un mensaje en el servidor.  <br/> ||
|LEAVE_ON_SERVER  <br/> |0 x 1  <br/> |
|REMOVE_AFTER  <br/> |0 x 2  <br/> |
|REMOVE_ON_NUKE  <br/> |0 x 4  <br/> |
|GET_REMOVE_AFTER_DAYS(UL)  <br/> |((ul)\>\>16)  <br/> |
|SET_REMOVE_AFTER_DAYS(days)  <br/> |((días)\<\<16)  <br/> |
   
## <a name="class-identifiers"></a>Identificadores de clase

Utilice la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Windows SDK para asociar el nombre simbólico GUID su valor.
  
{ed475410-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkAccountManager, 0xed475410, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76); 
  
{ed475411-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkPOP3Account, 0xed475411, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76);
  
{ed475412-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkIMAP4Account, 0xed475412, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76);
  
{ed475414-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkMAPIAccount, 0xed475414, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76);
  
{ed475418-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkMail, 0xed475418, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76);
  
{ed475419-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkAddressBook, 0xed475419, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76);
  
{ed475420-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkStore, 0xed475420, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76);
  
{4db5cbf0-3b77-4852-bc8e-bb81908861f3}
  
DEFINE_GUID (CLSID_OlkHotmailAccount, 0x4db5cbf0, 0x3b77, 0x4852, 0xbc, 0x8e, 0xbb, 0 x 81, 0 x 90, 0 x 88, 0 x 61, 0xf3);
  
{4db5cbf2-3b77-4852-bc8e-bb81908861f3}
  
DEFINE_GUID (CLSID_OlkLDAPAccount, 0x4db5cbf2, 0x3b77, 0x4852, 0xbc, 0x8e, 0xbb, 0 x 81, 0 x 90, 0 x 88, 0 x 61, 0xf3);
  
## <a name="interface-identifiers"></a>Identificadores de interfaz

Utilice la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Windows SDK para asociar el nombre simbólico GUID su valor.
  
{9240A6C0-AF41-11d2-8C3B-00104B2A6676}
  
DEFINE_GUID (IID_IOlkErrorUnknown, 0x9240a6c0, 0xaf41, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76);
  
{9240A6C1-AF41-11d2-8C3B-00104B2A6676}
  
DEFINE_GUID (IID_IOlkEnum, 0x9240a6c1, 0xaf41, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76);
  
{9240a6c3-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountNotify, 0x9240a6c3, 0xaf41, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76);
  
{9240a6cb-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountHelper, 0x9240a6cb, 0xaf41, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76); 
  
{9240a6cd-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountManager, 0x9240a6cd, 0xaf41, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76); 
  
{9240a6d2-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccount, 0x9240a6d2, 0xaf41, 0x11d2, 0x8c, 0x3b, 0 x 0, 0 x 10, 0x4b, 0x2a, 0x66, 0x76);
  

