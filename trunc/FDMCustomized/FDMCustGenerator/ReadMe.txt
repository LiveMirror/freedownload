I. ����� �������� ����������.

��������� ������������ ���������� �� �����:

�) �������� ������� ������.
�) ��������� ���������� ������������ ��� ���� ������.
�) ��������� ������������
�) �������� ������.

II. �������� �������.

FDMCS_SESSION FDMCSAPI fdmcsCreateSession (int iEdition)
������� ������. iEdition ������ ����� ���� �� ��������� ��������:
FDMCS_FREE, FDMCS_STANDARD, FDMCS_PROFESSIONAL, � ����������� ��
�������� ��������.

void FDMCSAPI fdmcsCloseSession (FDMCS_SESSION pS)
������� ������, ��������� ��� ������� �������.

void FDMCSAPI fdmcsSet_PrimaryID (FDMCS_SESSION pS, int iID)
���������� Primary ID.

void FDMCSAPI fdmcsSet_SiteURL (FDMCS_SESSION pS, LPCSTR pszURL)
���������� ���� �� ���� �������.

void FDMCSAPI fdmcsSet_SiteTitle (FDMCS_SESSION pS, LPCSTR pszTitle)
���������� �������� ����� �������.

void FDMCSAPI fdmcsSet_SiteIcon (FDMCS_SESSION pS, LPCSTR pszIcon)
���������� ���� � ������ ����� �������. ����� ������ ���� 16�16. 
pszIcon - ������ ���� � �����.

void FDMCSAPI fdmcsSet_Button (FDMCS_SESSION pS, BOOL bShowButton,
	LPCSTR pszIcon, LPCSTR pszText, LPCSTR pszURL)
���������� ��������� ������ �������. 
bShowButton - ���������� ������ ��� ���. ���� ����� FALSE, �� ��� 
��������� ��������� ������������.
pszIcon - ���� � ������ ��� ������ (32�32).
pszText - ����� ������.
pszURL  - URL ������.

void FDMCSAPI fdmcsSet_SetHomePage (FDMCS_SESSION pS, int iSet)
��������/��������� ��������� �������� �������� �� ���� �������.
iSet ����� ����: FDMCS_NO - �� �������������,
FDMCS_OPT_IN - �������� �����, �� ������������� ��-���������,
FDMCS_OPT_OUT - �������� �����, ������������� ��-���������.

void FDMCSAPI fdmcsSet_AddLinkToFavorites (FDMCS_SESSION pS, int iSet) 
��������� ��� ��� ������ �� ���� ������� � ���������.
iSet, ������ ��������� ���� ��������, ����� ��������� ����� ��������
FDMCS_YES - ����������, �� ��������� ������������.

void FDMCSAPI fdmcsSet_AddLinkToStartMenu (FDMCS_SESSION pS, int iSet)
��������� ��� ��� ������ �� ���� ������� � ���� ����.
�������� iSet ������ ����.

void FDMCSAPI fdmcsSet_IEButton (FDMCS_SESSION pS, int iSet, LPCSTR pszIcon)
��������� ��� ��� ������, ����������� �� ���� �������, � Internet Explorer.
�������� iSet ������ ����.
pszIcon - ���� � ������ ��� ������ (20�20).
����������. �� ��������, ���� ��� �������� FDMCS_STANDARD.

void FDMCSAPI fdmcsSet_GetCustVerBtn (FDMCS_SESSION pS, BOOL bShow)
��������/��������� ����� ������, ������������� custom ������ FDM'a.

void FDMCSAPI fdmcsAdd_Banner (FDMCS_SESSION pS, LPCSTR pszURL, LPCSTR pszImage)
�������� ������. 
pszURL - URL �������.
pszImage - ���� � ����� � ��������� ��� �������.
����������. �� ��������, ���� ��� �������� FDMCS_STANDARD.

void FDMCSAPI fdmcsAdd_Download (FDMCS_SESSION pS, LPCSTR pszURL, LPCSTR pszComment, BOOL bAutoStart)
�������� URL � ������ ������� ����� ���������.
pszURL - URL �������.
pszComment - ����������� � �������.
bAutoStart - ���������� ��� ��� ������� ������������� ����� ������� FDM'a.
����������. �� ��������, ���� ��� �������� FDMCS_STANDARD.

BOOL FDMCSAPI fdmcsGenerateDistrib (FDMCS_SESSION pS, LPCSTR pszFile, LPSTR pszErrDesc)
������� ����������� � ��������� �����������.
pszFile - �������� ���� ������������.
pszErrDesc - �������� ������, ���� ������� ����� ��������.
���������� TRUE � ������ ��������� �������� ������������.
����������. ��� ��������� ���������� ������ ������ ������� �������, 
����� ������� ���������� �������� ���� ����������� �� ����������, ����������
������ DLL.

III. ��������� ����������� ����������.

������ ������ ������� - ����������� Windows (WINAPI).
������� - ����������� C++.

// calling convension
#define FDMCSAPI WINAPI

// FDM session
typedef long FDMCS_SESSION;

// Edition type
#define FDMCS_FREE		0
#define FDMCS_STANDARD		1
#define FDMCS_PROFESSIONAL	2

// Options
#define FDMCS_NO		0
#define FDMCS_OPT_IN		1
#define FDMCS_OPT_OUT		2
#define FDMCS_YES		3

IV. �������������� �����.

fdmcs_PreExe.exe - ����-����������� ���������� ������������.
fdmcs_Inst_woa.exe - ����������� FDM'a ��� adware (��� Standard � Professional ��������).
fdmcs_Inst_wa.exe  - ����������� FDM'a c adware (��� Free ��������).